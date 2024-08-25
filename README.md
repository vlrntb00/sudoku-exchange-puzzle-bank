# Sudoku Exchange "Puzzle Bank"

This repository contains several hundred thousand Sudoku puzzles that were
computer generated for use by the [Sudoku Exchange](https://sudokuexchange.com/)
web site.

The puzzles were generated using the
[QQWing Sudoku](https://github.com/stephenostermiller/qqwing) software, which
ensure that each puzzle has a unique solution.
The generated puzzles were then graded using
[Sukaku Explainer](https://github.com/SudokuMonster/SukakuExplainer) and
sorted into four 'buckets':

| Filename            | Difficulty Rating |
| ------------------- | ----------------- |
| [easy.txt][1]       | < 1.5             |
| [medium.txt][2]     | < 2.5             |
| [hard.txt][3]       | < 5.0             |
| [diabolical.txt][4] | ≥ 5.0             |

Each text file has one puzzle per line, represented as three space-separated
fields and a Unix-style line-ending, for a total of 100 bytes per record:

     12 bytes of SHA1 hash of the digits string (for randomising order)
     81 bytes of puzzle digits
      4 bytes of rating (nn.n)
      3 bytes of white-space (including the linefeed);
    100 bytes total

### License

The data set is dedicated to the [public domain](LICENSE.txt).

[1]: https://github.com/grantm/sudoku-exchange-puzzle-bank/raw/master/easy.txt
[2]: https://github.com/grantm/sudoku-exchange-puzzle-bank/raw/master/medium.txt
[3]: https://github.com/grantm/sudoku-exchange-puzzle-bank/raw/master/hard.txt
[4]: https://github.com/grantm/sudoku-exchange-puzzle-bank/raw/master/diabolical.txt

### Summary

```
1.0: Last value in block, row or column
1.2: Hidden Single in block
1.5: Hidden Single in row or column
1.7: Direct Pointing
1.9: Direct Claiming
2.0: Direct Hidden Pair
2.3: Naked Single
2.5: Direct Hidden Triplet
2.6: Pointing
2.8: Claiming
3.0, 3.2, 3.4: Naked Pair, X-Wing, Hidden Pair
3.6, 3.8, 4.0: Naked Triplet, Swordfish, Hidden Triplet
4.2, 4.4: XY-Wing, XYZ-Wing
4.5 - 5.0: Unique rectangles and loops
5.0, 5.2, 5.4: Naked Quad, Jellyfish, Hidden Quad
5.6 - 6.0: Bivalue Universal Graves
6.2: Aligned Pair Exclusion
6.5-6.9: X-chains/X-cycles (common 6.5-6.8; rare 6.9)
6.6-7.0: Y-cycles (common 6.6-6.8; rare 6.9-7.0)
7.0-8.0: Bidirectional Cycles (common 7.0-7.2; rare 7.3+)
7.1-7.5: Forcing Chains (common 7.1-7.3; rare 7.4-7.5)
7.5: Aligned Triplet Exclusion
7.6-8.1: Nishio (common 7.6 and 7.8; semi-rare 7.7 and 7.9; rare 8.0-8.1)
8.2-8.7: Cell/Region Forcing Chains (common 8.2-8.5 (8.2 only for region); rare 8.6-8.7)
8.8-9.6: Dynamic Forcing Chains (common 8.8-9.4; rare 8.7 and 9.5(9.6?))
9.1-10.1: Dynamic Forcing Chains(+) (common 9.4-10.1; rare 9.3 and 10.2; ?9.1-9.2)
9.9-11.0: Dynamic Forcing Chains(+Forcing Chains) (common 10.2-10.7;
          rare 10.1 and 10.8 - 11.0; ultra rare 9.9-10.0)
10.8-11.5?: Dynamic Forcing Chains(+Multiple Forcing Chains) 
11.4-11.9: Dynamic Forcing Chains(+Dynamic Forcing Chains) 12.0-12.7(Pencilmarks)
```
