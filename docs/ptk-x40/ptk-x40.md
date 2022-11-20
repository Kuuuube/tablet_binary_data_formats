# PTK-x40

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

|   |  #7 |    #6    |     #5     |  #4 |     #3    |  #2 |  #1 |  #0 |
|:-:|:---:|:--------:|:----------:|:---:|:---------:|:---:|:---:|:---:|
| 0 |  0  |     0    |      0     |  0  |     0     |  0  |  1  |  0  |
| 1 |  1  | Proxmity | ReportFlag |  0  | MouseFlag |  B1 |  B0 |  P0 |
| 2 | X16 |    X15   |     X14    | X13 |    X12    | X11 | X10 |  X9 |
| 3 |  X8 |    X7    |     X6     |  X5 |     X4    |  X3 |  X2 |  X1 |
| 4 | Y16 |    Y15   |     Y14    | Y13 |    Y12    | Y11 | Y10 |  Y9 |
| 5 |  Y8 |    Y7    |     Y6     |  Y5 |     Y4    |  Y3 |  Y2 |  Y1 |
| 6 | P10 |    P9    |     P8     |  P7 |     P6    |  P5 |  P4 |  P3 |
| 7 |  P2 |    P1    |    SXt6    | Xt5 |    Xt4    | Xt3 | Xt2 | Xt1 |
| 8 | Xt0 |   SYt6   |     Yt5    | Yt4 |    Yt3    | Yt2 | Yt1 | Yt0 |
| 9 |  H5 |    H4    |     H3     |  H2 |     H1    |  H0 |  X0 |  Y0 |

### Art Pen Report

Untested but likely similar to [PTZ-x3xx Marker Report](../ptz-x3xx/ptz-x3xx.md#marker-report)

### Mouse Report

|   |  #7 |    #6    |     #5     |  #4 |     #3    |  #2 |  #1 |  #0 |
|:-:|:---:|:--------:|:----------:|:---:|:---------:|:---:|:---:|:---:|
| 0 |  0  |     0    |      0     |  0  |     0     |  0  |  1  |  0  |
| 1 |  1  | Proxmity | ReportFlag |  0  | MouseFlag |  1  |  0  |  0  |
| 2 | X16 |    X15   |     X14    | X13 |    X12    | X11 | X10 |  X9 |
| 3 |  X8 |    X7    |     X6     |  X5 |     X4    |  X3 |  X2 |  X1 |
| 4 | Y16 |    Y15   |     Y14    | Y13 |    Y12    | Y11 | Y10 |  Y9 |
| 5 |  Y8 |    Y7    |     Y6     |  Y5 |     Y4    |  Y3 |  Y2 |  Y1 |
| 6 |  0  |     0    |      0     |  B4 |     B3    |  B2 |  B1 |  B0 |
| 7 |  Sf |    Sb    |    SXt6    | Xt5 |    Xt4    | Xt3 | Xt2 | Xt1 |
| 8 | Xt0 |   SYt6   |     Yt5    | Yt4 |    Yt3    | Yt2 | Yt1 | Yt0 |
| 9 |  H5 |    H4    |     H3     |  H2 |     H1    |  H0 |  X0 |  Y0 |

### Aux Report

|   |    #7    |  #6 |  #5 |  #4 |  #3 |  #2 |  #1 |  #0 |
|:-:|:--------:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 0 |     0    |  0  |  0  |  0  |  1  |  1  |  0  |  0  |
| 1 | RingFlag | Ri6 | Ri5 | Ri4 | Ri3 | Ri2 | Ri1 | Ri0 |
| 2 |     0    |  0  |  0  |  0  |  0  |  0  |  0  | Rib |
| 3 |    B7    |  B6 |  B5 |  B4 |  B3 |  B2 |  B1 |  B0 |
| 4 |     0    |  0  |  0  |  0  |  0  |  0  |  0  |  0  |
| 5 |     0    |  0  |  0  |  0  |  0  |  0  |  0  |  0  |
| 6 |     0    |  0  |  0  |  0  |  0  |  0  |  0  |  0  |
| 7 |     0    |  0  |  0  |  0  |  0  |  0  |  0  |  0  |
| 8 |     0    |  0  |  0  |  0  |  0  |  0  |  0  |  0  |
| 9 |     0    |  0  |  0  |  0  |  0  |  0  |  0  |  0  |

## Key

- Byte 0 = `00001100` for Aux Reports, `00000010` otherwise

- Proximity = 1 when a tool is inside proximity, 0 otherwise

- ReportFlag = 1 when the report is a Mouse or Pen Report, 0 otherwise

- ToolReportFlag = 1 when the report is a Tool Report, 0 otherwise

    When ToolReportFlag is 1, ReportFlag will always be 0

- T = Tool

    Grip Pen = `10000000 0010`

    Grip Pen Eraser = `10000000 1010`

    Classic Pen = `10000000 0010`

    Classic Pen Eraser = `10000000 1010`

    Pro Pen = `10000000 0010`

    Pro Pen Eraser = `10000000 1010`

    Airbrush = `10010000 0010`

    Airbrush Eraser = `10010000 1010`

    Art Pen = `10000000 0100`

    Art Pen Eraser = `10000000 1100`

    Inking Pen = `10000000 0010`

    Mouse = `10000000 0110`

    Lens Cursor = `00000000 0110`

- Ser = Serial number

- MouseFlag = 1 when the report is a Mouse Report, 0 otherwise

- B = Button data

    `Pen Report`: B0 = bottom pen side button, B1 = top pen side button

    `Mouse Report`: B0 = front left, B1 = front middle, B2 = front right, B3 = back left, B4 = back right

    `Aux Report`: (From top to bottom) B0 = first button, B1 = second button, B2 = third button, B3 = fourth button, B4 = fifth button, B5 = sixth button, B6 = seventh button, B7 = eighth button

- X = X coordinate

- Y = Y coordinate

- P = Pressure data

- SXt = 0 when tilt is negative (tilted left), 1 when tilt is positive (tilted right)

    This bit should also be used as the most significant tilt value bit, then the tilt should be subtracted by half the maximum to split the tilt into positive or negative. It should likely only be used to determine when the tilt is positive/negative in cases where direction matters but exact tilt does not.

- Xt = Tilt value in X direction

- SYt = 0 when tilt is negative (tilted backwards), 1 when tilt is positive (tilted forwards)

    This bit should also be used as the most significant tilt value bit, then the tilt should be subtracted by half the maximum to split the tilt into positive or negative. It should likely only be used to determine when the tilt is positive/negative in cases where direction matters but exact tilt does not.

- Yt = Tilt value in Y direction

- H = Hover distance

    Higher when a tool is far from the tablet

    Lower when a tool is close to the tablet

- Sf = 1 when scrolling forward, 0 otherwise

- Sb = 1 when scrolling backwards, 0 otherwise

- RingFlag = 1 when the touch ring is in use, 0 otherwise

- Ri = Touch ring value, 0 or max when touching the left middle

    Max touch ring value is `1000111`. Not all bits are 1 when the max is reached.

    Touch ring value increases moving clockwise and decreases moving counterclockwise.

- Rib = Touch ring button data

    The button in the middle of the touch ring. Functions the exact same as other buttons.