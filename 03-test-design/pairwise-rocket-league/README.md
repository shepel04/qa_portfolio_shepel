# Pairwise testing · Rocket League

[← Back to test design](../README.md)

**Idea:** most bugs are caused by one parameter or by an interaction of **two** parameters.
So instead of all combinations, we make sure that **every pair of values appears together at least once**.

## Parameters (3-4-4-2)

| Game mode | Car body | Arena | Playlist |
|---|---|---|---|
| Duel (1v1) | Octane | DFH Stadium | Casual |
| Doubles (2v2) | Dominus | Mannfield | Competitive |
| Standard (3v3) | Fennec | Champions Field | |
| | Breakout | Urban Central | |

## Number of test cases

| | Formula | Cases |
|---|---|---|
| All combinations | 3 × 4 × 4 × 2 | **96** |
| Pairwise | 4 × 4 (two largest groups) | **16** |

Car body × Arena alone gives 16 unique pairs, and one test run holds only one such pair,
so 16 is the minimum. Game mode and Playlist are placed into these 16 runs so their pairs are covered too.

## Solution

| # | Car body | Arena | Game mode | Playlist |
|---|---|---|---|---|
| 1 | Octane | DFH Stadium | Duel (1v1) | Casual |
| 2 | Octane | Mannfield | Doubles (2v2) | Competitive |
| 3 | Octane | Champions Field | Standard (3v3) | Competitive |
| 4 | Octane | Urban Central | ~ | Casual |
| 5 | Dominus | DFH Stadium | Doubles (2v2) | Casual |
| 6 | Dominus | Mannfield | Duel (1v1) | Competitive |
| 7 | Dominus | Champions Field | ~ | Competitive |
| 8 | Dominus | Urban Central | Standard (3v3) | Casual |
| 9 | Fennec | DFH Stadium | Standard (3v3) | Competitive |
| 10 | Fennec | Mannfield | ~ | Casual |
| 11 | Fennec | Champions Field | Duel (1v1) | Casual |
| 12 | Fennec | Urban Central | Doubles (2v2) | Competitive |
| 13 | Breakout | DFH Stadium | ~ | Competitive |
| 14 | Breakout | Mannfield | Standard (3v3) | Casual |
| 15 | Breakout | Champions Field | Doubles (2v2) | Casual |
| 16 | Breakout | Urban Central | Duel (1v1) | Competitive |

`~` - any value: all pairs for this cell are already covered by other rows.

📄 [pairwise.xlsx](pairwise.xlsx) · [Google Sheets](https://docs.google.com/spreadsheets/d/1YwYVJbzzYSanFifmXo1UiStdeNZvo067SmT_NqpbhKs/edit)
