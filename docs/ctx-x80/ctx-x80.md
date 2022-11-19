# CTx-x80

## Format

Each cell is one bit, rows are byte numbers, and columns are bit numbers from MSB to LSB.

### Pen Report

|   |  #7 |  #6 |     #5    |  #4 |   #3   |  #2 | #1 | #0 |
|:-:|:---:|:---:|:---------:|:---:|:------:|:---:|:--:|:--:|
| 0 |  0  |  0  |     0     |  0  |    0   |  0  |  1 |  0 |
| 1 |  1  |  1  | Proximity |  ?  | Eraser |  B2 | B1 | B0 |
| 2 |  X7 |  X6 |     X5    |  X4 |   X3   |  X2 | X1 | X0 |
| 3 | X15 | X14 |    X13    | X12 |   X11  | X10 | X9 | X8 |
| 4 |  Y7 |  Y6 |     Y5    |  Y4 |   Y3   |  Y2 | Y1 | Y0 |
| 5 | Y15 | Y14 |    Y13    | Y12 |   Y11  | Y10 | Y9 | Y8 |
| 6 |  P7 |  P6 |     P5    |  P4 |   P3   |  P2 | P1 | P0 |
| 7 |  0  |  0  |     0     |  0  |    0   |  0  | P9 | P8 |
| 8 |  0  |  0  |     H5    |  H4 |   H3   |  H2 | H1 | H0 |
| 9 |  0  |  0  |     0     |  0  |    0   |  0  |  0 |  0 |

### Aux Report

Note: The aux report should also contain touch data. Touch data is currently untested. An aux report is also sent when a pen is detected. The report appears to contain no useable data when triggered in that way. 

|    | #7 | #6 | #5 | #4 | #3 | #2 | #1 | #0 |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
|  0 |  0 |  0 |  0 |  0 |  0 |  0 |  1 |  0 |
|  1 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  1 |
|  2 |  1 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
|  3 |  0 |  0 |  0 |  0 | B3 | B2 | B1 | B0 |
|  4 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
|  5 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
|  6 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
|  7 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
|  8 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
|  9 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 10 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 11 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 12 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 13 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 14 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 15 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 16 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 17 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 18 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 19 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 20 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 21 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 22 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 23 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 24 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 25 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 26 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 27 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 28 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 29 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 30 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 31 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 32 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 33 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 34 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 35 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 36 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 37 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 38 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 39 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 40 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 41 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 42 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 43 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 44 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 45 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 46 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 47 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 48 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 49 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 50 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 51 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 52 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 53 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 54 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 55 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 56 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 57 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 58 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 59 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 60 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 61 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 62 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 63 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 64 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |

## Key

- Proximity = 1 when a tool is inside proximity, 0 otherwise

- ? = Changes depending on the pen or pen side active for unknown reasons

- Eraser = 1 when the eraser is active, 0 otherwise

- H = Hover distance

    Higher when a tool is far from the tablet

    Lower when a tool is close to the tablet

- B = Button data

    `Pen Report`: B0 = bottom pen side button, B1 = top pen side button

    `Aux Report`: B0 = Top left tablet button, B1 = Bottom left tablet button, B2 = Top right tablet button, B3 = Top left tablet button

- X = X coordinate

- Y = Y coordinate

- P = Pressure data

- H = Hover distance

    Lower when a tool is far from the tablet

    Higher when a tool is close to the tablet