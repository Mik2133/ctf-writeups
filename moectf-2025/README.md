# MoeCTF 2025 — Writeups

Writeups for **MoeCTF 2025**, a Chinese university-level CTF hosted on `ctf.xidian.edu.cn`.

These notes were originally written in Chinese while solving the challenges and have been translated and reorganised into English. Screenshots are taken from the original solve document.

## Index

### Misc

| Challenge | Technique | Flag |
|---|---|---|
| [Misc Primer](misc/misc-primer.md) | Warm-up (incomplete) | — |
| [2048 Master](misc/2048-master.md) | Game state manipulation | `moectf{Y0u_4re_a_2048_m4st3r!!!!r0erowhu}` |
| [Pyjail 0](misc/pyjail-0.md) | Python jail / environment variables | `moectf{5dfc13b5-…}` |
| [Rush](misc/rush.md) | GIF frames + QR error correction | `moectf{QR_C0d3s_feATUR3_eRror_c0RRECt10N}` |
| [ez_LSB](misc/ez-lsb.md) | LSB / channel steganography | `moectf{LSB_1s_s0_1nt3rest1ng!!sj9wd}` |
| [ez_锟斤拷????](misc/ez-encoding.md) | GBK/UTF-8 mojibake | `moectf{EnC0d1ing_gbK_@nD_Utf_8_1s_4un!!ewwww}` |
| [weird_photo](misc/weird-photo.md) | PNG height restoration | `moectf{Image_Height_Restored}` |
| [encrypted_pdf](misc/encrypted-pdf.md) | Weak PDF password + layers | `moectf{Pdf_1s_r3a1ly_c0lor4ul!!ihdw}` |
| [哈基米难没露躲](misc/hachimi.md) | Zero-width steganography | `moectf{1b8956b9-…}` |
| [捂住一只耳](misc/hold-one-ear.md) | Stereo channels + Morse | `moectf{HALF_RADIO_IN_XDU}` |
| [Enchantment](misc/enchantment.md) | Packet capture (incomplete) | — |

Full flags are written at the top of each page.

## Coverage

- 11 Misc challenges are documented.
- Two entries are incomplete: `Misc Primer` is a sign-in warm-up with no recorded solve, and `Enchantment` stops after identifying the attachment as a packet capture containing a PNG upload.

## Categories at a glance

- **Misc** — game state, Python jails, GIF/QR reconstruction, LSB and channel steganography, encoding, PNG structure, PDF, zero-width text, audio channels, network forensics

## License

The text is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
