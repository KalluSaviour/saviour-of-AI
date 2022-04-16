## Aim: - Implementation of Toy Problem, Example - Implementation of water jug problem

## Algorithm:-

| Rule  | State            | Process                                                                 |
|-------|------------------|-------------------------------------------------------------------------|
| 1     | (X, Y ; X<4)     | (4, Y)                                                                  |
|       |                  | (Fill 4-gallon jug)                                                     |
| 2     | (X, Y ; Y<3)     | (X, 3)                                                                  |
|       |                  | (Fill 3-gallon jug)                                                     |
| 3     | (X, Y ; X>0)     | (0, Y)                                                                  |
|       |                  | (Empty 4-gallon jug)                                                    |
| 4     | (X, Y ; Y>0)     | (X, 0)                                                                  |
|       |                  | (Empty 3-gallon jug)                                                    |
| 5     | (X, Y ; X+Y>=4 ^ | (4, Y - (4 - X))                                                        |
|       |  Y>0)            | (Pour water from 3-gallon jug into 4-gallon until 4-gallon jug is full) |
| 6     | (X, Y ; X+Y>=3 ^ | (X-(3-Y), 3)                                                            |
|       |  X>0)            | (Pour water from 4-gallon jug into 3-gallon until 3-gallon jug is full) |
| 7     | (X, Y ; X+Y<=4 ^ | (X+Y, 0)                                                                |
|       |  Y>0)            | (Pour all water from 3-gallon jug into 4-gallon jug)                    |
| 8     | (X, Y ; X+Y<=3 ^ | (0, X+Y)                                                                |
|       |  X>0)            | (Pour all water from 4-gallon jug into 3-gallon jug)                    |
| 9     | (0, 2)           | (2, 0)                                                                  |
|       |                  | (Pour 2 gallon water from 3 gallon jug into 4 gallon jug)               |


Replace ; with |
