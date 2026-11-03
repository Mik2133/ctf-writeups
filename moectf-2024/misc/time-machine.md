# Time Machine

| | |
|---|---|
| **Event** | MoeCTF 2024 |
| **Category** | Misc — OSINT |
| **Flag** | `moectf{han_fang_tang}` |

## Overview

An OSINT challenge built around a historical photo and a nearby location.

![The challenge image](../assets/time-machine/image94.png)

The hint is simply: *notice the hint*.

## Solution

### 1. Identify the landmark

Entering the clue into a search engine leads to **Wang Jian's tomb** (the Yongling Museum) in Chengdu.

![Search result identifying the tomb](../assets/time-machine/image95.png)
![Search result identifying the tomb](../assets/time-machine/image96.png)
![Search result identifying the tomb](../assets/time-machine/image97.png)

The modern map around the tomb confirms the layout.

![Verifying the location on the map](../assets/time-machine/image98.png)
![Verifying the location on the map](../assets/time-machine/image99.png)

### 2. Identify the building

Zooming in on the map shows two traditional-medicine pharmacies in the area, so there is ambiguity. My first guess was:

```
moectf{bing_an_tang}
```

That was rejected.

![Wrong first guess](../assets/time-machine/image100.png)
![The other nearby pharmacy](../assets/time-machine/image101.png)

Trying the second one:

```
moectf{han_fang_tang}
```

This is the accepted flag.

## Takeaways

- When a map shows two plausible candidates, submit both — the checker distinguishes them.
- The pinyin spelling matters: flags use the standard pinyin of the business name, with underscores between syllables.
- "Notice the hint" usually means the hint is embedded in the image itself, not in the challenge text.
