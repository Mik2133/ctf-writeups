# 哈基米难没露躲

| | |
|---|---|
| **Event** | MoeCTF 2025 |
| **Category** | Misc — zero-width steganography |
| **Flag** | `moectf{1b8956b9-a423-4101-a1bd-65be33682c82}` |

## Overview

The attached image renders as visibly corrupted — the challenge title is a joke about the author having eaten a hallucinogenic mushroom. The corruption is the first clue that the file is more than an image.

![The corrupted image preview](../assets/hachimi/image1.png)

## Solution

Opening the file in 010 Editor revealed an embedded hint string:

![The file in 010 Editor](../assets/hachimi/image2.png)
![The embedded txthint string](../assets/hachimi/image3.png)

```
txthint{https://lhlnb.top/hajimi/base64}
```

Searching for the URL was not useful (the search engine was failing at the time), and it quickly became clear that this was not asking us to open a web page.

![The search dead end](../assets/hachimi/image4.png)

Treating it as a Base64 or URL-encoding instruction in CyberChef did not produce anything meaningful either.

![The CyberChef attempt](../assets/hachimi/image5.png)

The hint was pointing at the encoding family, not at a remote payload. The text itself contains invisible zero-width characters, so a normal Base64 decode sees only the visible glyphs.

![The text carrying invisible characters](../assets/hachimi/image6.png)

Using an online zero-width steganography decoder extracted the hidden message immediately.

![The zero-width decode result](../assets/hachimi/image7.png)

```
moectf{1b8956b9-a423-4101-a1bd-65be33682c82}
```

## Takeaways

- Text that looks empty or oddly spaced may be carrying zero-width characters — inspect the code points, not the glyphs.
- A hint containing a URL is not always an instruction to fetch it; read what the path or filename is telling you.
