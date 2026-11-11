# 2048 Master

| | |
|---|---|
| **Event** | MoeCTF 2025 |
| **Category** | Misc — game state manipulation |
| **Flag** | `moectf{Y0u_4re_a_2048_m4st3r!!!!r0erowhu}` |

## Overview

The attachment is a small playable 2048 game. Playing normally for a couple of rounds is enough to make the challenge's hint appear.

## Solution

After a few moves the game printed a hint asking for a **16384** tile. Around the same time a new file, `layout.dat`, appeared next to the game.

Opening it in a hex editor shows the board state stored as powers of two:

```
2 4 8 16 32 ...
```

The obvious move is to edit the file directly and put 16384 on the board instead of grinding for it. My first two edits had no effect — I had not written the value to the slot the game actually reads on load.

After correcting the offset and saving, the game still did not react immediately; it only re-read the layout after one more move in-game. That extra move triggered the win check and the flag was displayed.

```
moectf{Y0u_4re_a_2048_m4st3r!!!!r0erowhu}
```

## Takeaways

- Games that persist their state to a plain file are state-manipulation targets, not just reverse-engineering targets.
- Editing the right value is only half the problem — the program must be made to reload it, often by performing one more normal action.
