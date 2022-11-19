# GD-xxxx-U

## Format

Each cell is one bit, rows are byte numbers, and columns are bit numbers from MSB to LSB.

### Tool Report

|   |   #7  |     #6    |     #5     |   #4  |   #3  |   #2  |       #1       |   #0  |
|:-:|:-----:|:---------:|:----------:|:-----:|:-----:|:-----:|:--------------:|:-----:|
| 0 |   0   |     0     |      0     |   0   |   0   |   0   |        1       |   0   |
| 1 |   1   | Proximity | ReportFlag |   0   |   0   |   0   | ToolReportFlag |   0   |
| 2 |  T11  |    T10    |     T9     |   T8  |   T7  |   T6  |       T5       |   T4  |
| 3 |   T3  |     T2    |     T1     |   T0  | Ser34 | Ser33 |      Ser32     | Ser31 |
| 4 | Ser30 |   Ser29   |    Ser28   | Ser27 | Ser26 | Ser25 |      Ser24     | Ser23 |
| 5 | Ser22 |   Ser21   |    Ser20   | Ser19 | Ser18 | Ser17 |      Ser16     | Ser15 |
| 6 | Ser14 |   Ser13   |    Ser12   | Ser11 | Ser10 |  Ser0 |      Ser9      |  Ser8 |
| 7 |  Ser7 |    Ser6   |    Ser5    |  Ser4 |  Ser3 |  Ser2 |      Ser1      |  Ser0 |
| 8 |   0   |     0     |      0     |   0   |   0   |   0   |        0       |   0   |
| 9 |   0   |     0     |      0     |   0   |   0   |   0   |        0       |   0   |

### Pen Report

|   | #7  | #6        | #5         | #4  | #3  | #2  | #1  | #0  |
|:-:|:---:|:---------:|:----------:|:---:|:---:|:---:|:---:|:---:|
| 0 | 0   | 0         | 0          | 0   | 0   | 0   | 1   | 0   |
| 1 | 1   | Proximity | ReportFlag | 0   | 0   | B1  | B0  | 0   |
| 2 | X15 | X14       | X13        | X12 | X11 | X10 | X9  | X8  |
| 3 | X7  | X6        | X5         | X4  | X3  | X2  | X1  | X0  |
| 4 | Y15 | Y14       | Y13        | Y12 | Y11 | Y10 | Y9  | Y8  |
| 5 | Y7  | Y6        | Y5         | Y4  | Y3  | Y2  | Y1  | Y0  |
| 6 | P9  | P8        | P7         | P6  | P5  | P4  | P3  | P2  |
| 7 | P1  | P0        | SXt6       | Xt5 | Xt4 | Xt3 | Xt2 | Xt1 |
| 8 | Xt0 | SYt6      | Yt5        | Yt4 | Yt3 | Yt2 | Yt1 | Yt0 |
| 9 | H4  | H3        | H2         | H1  | H0  | 0   | 0   | 0   |

### Mouse Report

Untested but likely matching [GD-xxxx-U](../gd-xxxx-u/gd-xxxx-u.md#mouse-report-0)

## Key

- Proximity = 1 when a tool is inside proximity, 0 otherwise

- ReportFlag = 1 when the report is a Mouse or Pen Report, 0 otherwise

- ToolReportFlag = 1 when the report is a Tool Report, 0 otherwise

    When ToolReportFlag is 1, ReportFlag will always be 0

- T = Tool

    Pen = `10000101 0010`

    Eraser = `10000101 1010`

    Mouse = Untested

- Ser = Serial number

- H = Hover distance

    Higher when a tool is far from the tablet

    Lower when a tool is close to the tablet

- B = Button data

    `Pen Report`: B0 = bottom pen side button, B1 = top pen side button

- X = X coordinate

- Y = Y coordinate

- P = Pressure data

- SXt = 0 when tilt is negative (tilted left), 1 when tilt is positive (tilted right)

    (Wacom's spec at the time these tablets were made likely flipped these. Above is how modern standards would define tilt negative vs positive.)

- Xt = Tilt value in X direction

- SYt = 0 when tilt is negative (tilted backwards), 1 when tilt is positive (tilted forwards)

    (Wacom's spec at the time these tablets were made likely flipped these. Above is how modern standards would define tilt negative vs positive.)

- Yt = Tilt value in Y direction