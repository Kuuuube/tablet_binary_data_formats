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
| 9 |   H4  |     H3    |     H2     |   H1  |   H0  |   0   |        0       |   0   |

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

### Mouse Report 0

|   | #7  | #6        | #5         | #4  | #3  | #2  | #1            | #0  |
|:-:|:---:|:---------:|:----------:|:---:|:---:|:---:|:-------------:|:---:|
| 0 | 0   | 0         | 0          | 0   | 0   | 0   | 1             | 0   |
| 1 | 1   | Proximity | ReportFlag | 0   | 1   | 0   | MouseReportId | 0   |
| 2 | X15 | X14       | X13        | X12 | X11 | X10 | X9            | X8  |
| 3 | X7  | X6        | X5         | X4  | X3  | X2  | X1            | X0  |
| 4 | Y15 | Y14       | Y13        | Y12 | Y11 | Y10 | Y9            | Y8  |
| 5 | Y7  | Y6        | Y5         | Y4  | Y3  | Y2  | Y1            | Y0  |
| 6 | Th9 | Th8       | Th7        | Th6 | Th5 | Th4 | Th3           | Th2 |
| 7 | Th1 | Th0       | 0          | 0   | 0   | 0   | 0             | 0   |
| 8 | 0   | 0         | B4         | B3  | Thd | B2  | B1            | B0  |
| 9 | H4  | H3        | H2         | H1  | H0  | 0   | 0             | 0   |

### Mouse Report 1

|   |  #7 |     #6    |     #5     |  #4 |  #3 |  #2 |       #1      | #0 |
|:-:|:---:|:---------:|:----------:|:---:|:---:|:---:|:-------------:|:--:|
| 0 |  0  |     0     |      0     |  0  |  0  |  0  |       1       |  0 |
| 1 |  1  | Proximity | ReportFlag |  0  |  1  |  0  | MouseReportId |  0 |
| 2 | X15 |    X14    |     X13    | X12 | X11 | X10 |       X9      | X8 |
| 3 |  X7 |     X6    |     X5     |  X4 |  X3 |  X2 |       X1      | X0 |
| 4 | Y15 |    Y14    |     Y13    | Y12 | Y11 | Y10 |       Y9      | Y8 |
| 5 |  Y7 |     Y6    |     Y5     |  Y4 |  Y3 |  Y2 |       Y1      | Y0 |
| 6 |  R9 |     R8    |     R7     |  R6 |  R5 |  R4 |       R3      | R2 |
| 7 |  R1 |     R0    |     Rd     |  0  |  0  |  0  |       0       |  0 |
| 8 |  0  |     0     |      0     |  0  |  0  |  0  |       0       |  0 |
| 9 |  H4 |     H3    |     H2     |  H1 |  H0 |  0  |       0       |  0 |

## Key

- Proximity = 1 when a tool is inside proximity, 0 otherwise

- ReportFlag = 1 when the report is a Mouse or Pen Report, 0 otherwise

- ToolReportFlag = 1 when the report is a Tool Report, 0 otherwise

    When ToolReportFlag is 1, ReportFlag will always be 0

- T = Tool

    Pen = `10000010 0010`

    Eraser = `10000010 1010`

    Mouse = `00001001 0100`

- Ser = Serial number

- H = Hover distance

    Higher when a tool is far from the tablet

    Lower when a tool is close to the tablet

- B = Button data

    `Pen Report`: B0 = bottom pen side button, B1 = top pen side button

    `Mouse Report 0`: B0 = front left, B1 = front middle, B2 = front right, B3 = back left, B4 = back right

- X = X coordinate

- Y = Y coordinate

- P = Pressure data

- SXt = 0 when tilt is negative (tilted left), 1 when tilt is positive (tilted right)

    This bit should also be used as the most significant tilt value bit, then the tilt should be subtracted by half the maximum to split the tilt into positive or negative. It should likely only be used to determine when the tilt is positive/negative in cases where direction matters but exact tilt does not.

- Xt = Tilt value in X direction

- SYt = 0 when tilt is negative (tilted backwards), 1 when tilt is positive (tilted forwards)

    This bit should also be used as the most significant tilt value bit, then the tilt should be subtracted by half the maximum to split the tilt into positive or negative. It should likely only be used to determine when the tilt is positive/negative in cases where direction matters but exact tilt does not.

- Yt = Tilt value in Y direction

- MouseReportId = 0 when using `Mouse Report 0`, 1 when using `Mouse Report 1`

    When using a mouse it will alternate between sending `Mouse Report 0` and `Mouse Report 1`. Typically, switching between them every time a report is sent, but sometimes more than one report of either will be sent in a row.

- Th = Thumbwheel value

- Thd = 0 when thumbwheel is rotated backwards, 1 when thumbwheel is rotated forwards

- R = Rotation value, 0 when the front of the tool is aligned with the front of the tablet. Max value when the front of the tool is aligned with the back of the tablet.

- Rd = 0 when when the front of the tool is pointing to the left side of the tablet at any angle, 1 when when the front of the tool is pointing to the right side of the tablet at any angle