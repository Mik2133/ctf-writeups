# Rush

| | |
|---|---|
| **Event** | MoeCTF 2025 |
| **Category** | Misc — GIF frame steganography / QR reconstruction |
| **Flag** | `moectf{QR_C0d3s_feATUR3_eRror_c0RRECt10N}` |

## Overview

The attachment is a GIF. Its metadata is unremarkable, but some keyframes visibly contain fragments of a QR code. That makes it an image-steganography problem rather than a plain animation.

## Solution

I stepped through the file in StegSolve, first checking individual colour channels and then individual frames.

The animation has **12 frames**. The QR codes are not simply placed in separate frames: because the frames flash quickly, what the eye sees is several codes superimposed by persistence of vision. Each frame therefore looks damaged, and no single frame decodes on its own with an online QR reader.

My first attempt — stacking the frames in PowerPoint — did not produce a readable code either.

The actual approach is to repair the codes using the redundancy QR codes are designed with: the payload survives partial corruption because of Reed–Solomon error correction. Once the frames were repaired rather than naively overlaid, the code decoded.

```
moectf{QR_C0d3s_feATUR3_eRror_c0RRECt10N}
```

## Takeaways

- Check frames *and* channels, but also check how the animation is meant to be perceived — flashing frames can encode data through persistence of vision.
- A QR code that looks broken is not necessarily unreadable; error correction tolerates a surprising amount of damage.
- Naively stacking frames is not the same as reconstructing the underlying code.
