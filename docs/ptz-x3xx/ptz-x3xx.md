# PTZ-x3xx

## Format

Each cell is one bit, rows are byte numbers, and columns are bit numbers from MSB to LSB.

### Tool Report

|   |   #7  |     #6    |     #5     |   #4  |   #3  |   #2  |       #1       |   #0  |
|:-:|:-----:|:---------:|:----------:|:-----:|:-----:|:-----:|:--------------:|:-----:|
| 0 |   0   |     0     |      0     |   0   |   0   |   0   |        1       |   0   |
| 1 |   1   | Proximity | ReportFlag |   0   |   0   |   0   | ToolReportFlag |   0   |
| 2 |  T11  |    T10    |     T9     |   T8  |   T7  |   T6  |       T5       |   T4  |
| 3 |   T3  |     T2    |     T1     |   T0  | Ser30 | Ser29 |      Ser28     | Ser27 |
| 4 | Ser26 |   Ser25   |    Ser24   | Ser23 | Ser22 | Ser21 |      Ser20     | Ser19 |
| 5 | Ser18 |   Ser17   |    Ser16   | Ser15 | Ser14 | Ser13 |      Ser12     | Ser11 |
| 6 | Ser10 |    Ser0   |    Ser9    |  Ser8 |  Ser7 |  Ser6 |      Ser5      |  Ser4 |
| 7 |  Ser3 |    Ser2   |    Ser1    |  Ser0 |   0   |   0   |        0       |   0   |
| 8 |   0   |     0     |      0     |   0   |   0   |   0   |        0       |   0   |
| 9 |   0   |     0     |      0     |   0   |   0   |   0   |        0       |   0   |

### Pen Report

|   |  #7 |    #6    |     #5     |     #4    |     #3     |  #2 |  #1 |  #0 |
|:-:|:---:|:--------:|:----------:|:---------:|:----------:|:---:|:---:|:---:|
| 0 |  0  |     0    |      0     |     0     |      0     |  0  |  1  |  0  |
| 1 |  1  | Proxmity | ReportFlag | MouseFlag | MarkerFlag |  B1 |  B0 |  0  |
| 2 | X15 |    X14   |     X13    |    X12    |     X11    | X10 |  X9 |  X8 |
| 3 |  X7 |    X6    |     X5     |     X4    |     X3     |  X2 |  X1 |  X0 |
| 4 | Y15 |    Y14   |     Y13    |    Y12    |     Y11    | Y10 |  Y9 |  Y8 |
| 5 |  Y7 |    Y6    |     Y5     |     Y4    |     Y3     |  Y2 |  Y1 |  Y0 |
| 6 |  P9 |    P8    |     P7     |     P6    |     P5     |  P4 |  P3 |  P2 |
| 7 |  P1 |    P0    |    SXt6    |    Xt5    |     Xt4    | Xt3 | Xt2 | Xt1 |
| 8 | Xt0 |   SYt6   |     Yt5    |    Yt4    |     Yt3    | Yt2 | Yt1 | Yt0 |
| 9 |  H7 |    H6    |     H5     |     H4    |     H3     |  H2 |  H1 |  H0 |

### Marker Report

|   |  #7 |    #6    |     #5     |     #4    |     #3     |  #2 | #1 | #0 |
|:-:|:---:|:--------:|:----------:|:---------:|:----------:|:---:|:--:|:--:|
| 0 |  0  |     0    |      0     |     0     |      0     |  0  |  1 |  0 |
| 1 |  1  | Proxmity | ReportFlag | MouseFlag | MarkerFlag |  0  |  1 |  0 |
| 2 | X15 |    X14   |     X13    |    X12    |     X11    | X10 | X9 | X8 |
| 3 |  X7 |    X6    |     X5     |     X4    |     X3     |  X2 | X1 | X0 |
| 4 | Y15 |    Y14   |     Y13    |    Y12    |     Y11    | Y10 | Y9 | Y8 |
| 5 |  Y7 |    Y6    |     Y5     |     Y4    |     Y3     |  Y2 | Y1 | Y0 |
| 6 |  R9 |    R8    |     R7     |     R6    |     R5     |  R4 | R3 | R2 |
| 7 |  R1 |    R0    |     Rd     |     0     |      0     |  0  |  0 |  0 |
| 8 |  0  |     0    |      0     |     0     |      0     |  0  |  0 |  0 |
| 9 |  H7 |    H6    |     H5     |     H4    |     H3     |  H2 | H1 | H0 |

### Mouse Report

|   |  #7 |    #6    |     #5     |     #4    |     #3     |  #2 | #1 | #0 |
|:-:|:---:|:--------:|:----------:|:---------:|:----------:|:---:|:--:|:--:|
| 0 |  0  |     0    |      0     |     0     |      0     |  0  |  1 |  0 |
| 1 |  1  | Proxmity | ReportFlag | MouseFlag | MarkerFlag |  0  |  0 |  0 |
| 2 | X15 |    X14   |     X13    |    X12    |     X11    | X10 | X9 | X8 |
| 3 |  X7 |    X6    |     X5     |     X4    |     X3     |  X2 | X1 | X0 |
| 4 | Y15 |    Y14   |     Y13    |    Y12    |     Y11    | Y10 | Y9 | Y8 |
| 5 |  Y7 |    Y6    |     Y5     |     Y4    |     Y3     |  Y2 | Y1 | Y0 |
| 6 |  0  |     0    |      0     |     0     |      0     |  0  |  0 |  0 |
| 7 |  0  |     0    |      0     |     0     |      0     |  0  |  0 |  0 |
| 8 |  0  |    B4    |     B3     |     B2    |     B1     |  B0 | Sf | Sb |
| 9 |  H7 |    H6    |     H5     |     H4    |     H3     |  H2 | H1 | H0 |

## Key

- Proximity = 1 when a tool is inside proximity, 0 otherwise

- ReportFlag = 1 when the report is a Mouse or Pen Report, 0 otherwise

- ToolReportFlag = 1 when the report is a Tool Report, 0 otherwise

    When ToolReportFlag is 1, ReportFlag will always be 0

- T = Tool

    Grip Pen = `10000010 0011`

    Grip Pen Eraser = `10000010 1011`

    Classic Pen = `10000001 0011`

    Classic Pen Eraser = `10000001 1011`

    Airbrush = `10010001 0011`

    Airbrush Eraser = `10010001 1011`

    Marker Pen = `10001000 0101`

    Inking Pen = `10000000 0001`

    2D Mouse = `00000001 0111`

    Lens Cursor = `00001001 0111`

- Ser = Serial number

- MouseFlag = 1 when the report is a Mouse Report, 0 otherwise

- MarkerFlag = 1 when the report is a Marker Report, 0 otherwise

    The marker pen alternates between sending Marker Reports and Pen Reports.

- B = Button data

    `Pen Report`: B0 = bottom pen side button, B1 = top pen side button

    `Mouse Report`: B0 = front left, B1 = front middle, B2 = front right, B3 = side left, B4 = side right

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

- Th = Thumbwheel value

- Thd = 0 when thumbwheel is rotated backwards, 1 when thumbwheel is rotated forwards

- R = Rotation value, 0 when the front of the tool is aligned with the right side of the tablet, Max value when the front of the tool is aligned with the left side of the tablet

    Max rotation is `11100001 00`. Not all bits are 1 when the max is reached.
    
    Rotation is half of the max when the front of the tool is aligned with the front or back of the tablet.

- Rd = 0 when when the front of the tool is pointing to the front of the tablet at any angle, 1 when when the front of the tool is pointing to the back of the tablet at any angle

- Sf = 1 when scrolling forward, 0 otherwise

- Sb = 1 when scrolling backwards, 0 otherwise