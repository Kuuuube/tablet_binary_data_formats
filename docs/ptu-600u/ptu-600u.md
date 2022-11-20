# PTU-600U

## Format

Each cell is one bit, rows are byte numbers, and columns are bit numbers from MSB to LSB.

### Pen Report

|   |  #7 |  #6 |     #5    |  #4 |  #3 |   #2   | #1 | #0 |
|:-:|:---:|:---:|:---------:|:---:|:---:|:------:|:--:|:--:|
| 0 |  0  |  0  |     0     |  0  |  0  |    0   |  1 |  0 |
| 1 |  0  |  0  | Proximity |  B3 |  B2 | Eraser | B1 | B0 |
| 2 |  X7 |  X6 |     X5    |  X4 |  X3 |   X2   | X1 | X0 |
| 3 | X15 | X14 |    X13    | X12 | X11 |   X10  | X9 | X8 |
| 4 |  Y7 |  Y6 |     Y5    |  Y4 |  Y3 |   Y2   | Y1 | Y0 |
| 5 | Y15 | Y14 |    Y13    | Y12 | Y11 |   Y10  | Y9 | Y8 |
| 6 |  P7 |  P6 |     P5    |  P4 |  P3 |   P2   | P1 | P0 |
| 7 |  0  |  0  |     0     |  0  |  0  |    0   |  0 | P8 |

## Key

- Proximity = 1 when a tool is inside proximity, 0 otherwise

- B = Button data

    `Pen Report`: B0 = pen tip, B1 = bottom pen side button, B2 = eraser tip, B3 = top pen side button

- Eraser = 1 when the eraser is active, 0 otherwise

- X = X coordinate

- Y = Y coordinate

- P = Pressure data