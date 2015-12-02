# N-puzzle solver

Solves the N-puzzle using IDA*. It always findes an optimal solution.

It is not recomended solving boards larger than 4 x 4 (which also might take quite some time depending on your hardware).

### Custom board
If you want to usa a custom board, edit the `CUSTOM_BOARD` variable on [line 6][1] to a sequence of the numbers in the board. The default is `None`, which generates a random board of the size specified in variable `DIMENSIONS` on [line 5][2].

Remember to update the variable `DIMENSIONS` on [line 5][2] to the correct dimensions. The default is 3 (which means a 3x3 board, i.e. the 8-puzzle)

If you want to solve a board larger than 4x4, you need to update the `MAX_DEPTH`-variable on [line 7][3] to the maximal number of moves required to solve the board (regardless of the configuration). See [this artice][4] for more information.

#### Example

If you want this board:

```
|13|3 |2 |14|
|9 |5 |4 |11|
|8 |6 |10|1 |
|15|12|7 |  |
```

You should change line 6 to: `CUSTOM_BOARD = [13, 3, 2, 14, 9, 5, 4, 11, 8, 6, 10, 1, 15, 12, 7]`

And line 5 to: `DIMENSIONS = 4`

[1]: https://github.com/boyebn/n-puzzle-solver/blob/master/n-puzzle-solver.py#L6
[2]: https://github.com/boyebn/n-puzzle-solver/blob/master/n-puzzle-solver.py#L5
[3]: https://github.com/boyebn/n-puzzle-solver/blob/master/n-puzzle-solver.py#L7
[4]: http://oeis.org/A087725
