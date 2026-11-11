# Enchantment

| | |
|---|---|
| **Event** | MoeCTF 2025 |
| **Category** | Misc — network forensics (incomplete) |
| **Flag** | Not recovered in the source notes |

## Overview

The attachment initially looks like an ordinary file with nothing interesting in it. The original notes describe it as unremarkable until the file type was checked more carefully.

![The attachment at first glance](../assets/enchantment/image1.png)
![Nothing obvious on inspection](../assets/enchantment/image2.png)

## Status

The material is not an image-steganography challenge as first assumed — it is a **packet capture**. The recorded traffic shows a PNG being uploaded, but the solve log stops at that observation.

![The traffic capture showing a PNG upload](../assets/enchantment/image3.png)

No extraction step or flag was recorded, so this writeup is kept for completeness rather than as a solution reference.
