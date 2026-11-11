# ez_LSB

| | |
|---|---|
| **Event** | MoeCTF 2025 |
| **Category** | Misc — LSB / channel steganography |
| **Flag** | `moectf{LSB_1s_s0_1nt3rest1ng!!sj9wd}` |

## Overview

An image that looks ordinary. There is no obvious crop or appended archive, so the data is likely inside the pixel values.

![The original image](../assets/ez-lsb/image1.png)

## Solution

StegSolve across the colour channels showed nothing at first.

![StegSolve channel inspection](../assets/ez-lsb/image2.png)

A Base64-looking string in the challenge material decoded to only half of a flag, which meant a second half was hidden somewhere.

![The Base64-looking string](../assets/ez-lsb/image3.png)
![Only half of a flag](../assets/ez-lsb/image4.png)

Comparing the image against the original revealed an extra white edge in the **red channel** that should not be there.

![Comparing against the original](../assets/ez-lsb/image5.png)
![The extra white edge in the red channel](../assets/ez-lsb/image6.png)

Zooming into that edge showed what looked like Morse code; my first reading produced

```
flag{hackitsecomasithistakes}
```

which was rejected.

![The Morse-like pattern in the white edge](../assets/ez-lsb/image7.png)
![Checking the Base64 payload again](../assets/ez-lsb/image8.png)

The Base64 string was the reliable path. Decoding

```
bW9lY3Rme0xTQl8xc19zMF8xbnQzcmVzdDFuZyEhc2o5d2R9
```

gave the complete flag:

![Decoding the full string in CyberChef](../assets/ez-lsb/image9.png)

```
moectf{LSB_1s_s0_1nt3rest1ng!!sj9wd}
```

## Takeaways

- A half-decoded flag is a hint that the data is split across carriers — keep looking instead of guessing the tail.
- Diff the image against a reference when one is available; a one-pixel white border is easy to miss at normal zoom.
- Morse readings from noise can look plausible and still be wrong; prefer a deterministic decode when one exists.
