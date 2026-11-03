# MoeCTF 2024 — Writeups

Writeups for **MoeCTF 2024**, a Chinese university-level CTF hosted on `ctf.xidian.edu.cn`.

These notes were originally written in Chinese while solving the challenges and have been translated and reorganised into English. Screenshots are kept from the original solve sessions.

## Index

### Misc

| Challenge | Technique | Flag |
|---|---|---|
| [Check-in](misc/check-in.md) | Warm-up / platform | `moectf{welcome_to_moectf!}` |
| [Abnormal Lag](misc/abnormal-lag.md) | Audio spectrogram | `moectf{09e3f7f8-…}` |
| [ez_Forensics](misc/ez-forensics.md) | Windows memory forensics (Volatility) | `moectf{WWBGY-TLVC5-XKYBZ}` |
| [So Many 'm'](misc/so-many-m.md) | Text frequency analysis | `moectf{c0MpuTaskingD4rE}` |
| [Misc Primer](misc/misc-primer.md) | Morse code | `moectf{H4VE_A_G00D_T1ME}` |
| [Luo Xiaohei](misc/luo-xiaohei.md) | GIF frame steganography | `moectf{y0uu6r3th3m0st3r1nth1sf13ld}` |
| [The Upside and Down](misc/upside-and-down.md) | Reversed file / PNG repair | `moectf{Fri3nds_d0n't_lie!}` |
| [ctf2077](misc/ctf2077.md) | Channel splitting (StegSolve) | `moectf{84d7f247-…}` |
| [ez_F5](misc/ez-f5.md) | JPEG F5 steganography + Base32 | `moectf{F5_15_s0_Intere5t1n9}` |
| [moejail_lv1](misc/moejail-lv1.md) | Python jail escape | `moectf{ah_ha-now_you_kn0w_…}` |
| [moejail_lv2](misc/moejail-lv2.md) | Python jail (incomplete) | — |
| [Hold One Ear](misc/hold-one-ear.md) | Audio + keyboard coordinates | `moectf{NEVERGETUP}` |
| [At Least 300 Per Person](misc/300-per-person.md) | QR code reassembly | `moectf{we1rd_qrc0d3}` |
| [Find It](misc/find-it.md) | OSINT / geolocation | `moectf{ji_di_bao_you_er_yuan}` |
| [the_secret_of_snowball](misc/secret-of-snowball.md) | JPEG repair + Base64 | `moectf{Welc0me_t0_the_secret_life_0f_Misc!}` |
| [My Layer Is Above Yours](misc/my-layer-above-yours.md) | Layered document + channel steganography | `moectf{d751894b-…}` |
| [Time Machine](misc/time-machine.md) | OSINT / map | `moectf{han_fang_tang}` |

### Web

| Challenge | Technique | Flag |
|---|---|---|
| [Sign In](web/sign-in.md) | WSRX instance + client-side task | `moectf{Thanks_For_You_signing_in_…}` |

### Pwn

| Challenge | Technique | Flag |
|---|---|---|
| [Binary Exploitation Primer](pwn/pwn-primer.md) | `nc` to a remote service | `moectf{Welcome_to_the_journey_of_Pwn}` |

### Reverse

| Challenge | Technique | Flag |
|---|---|---|
| [dynamic](reverse/dynamic.md) | PE recon (incomplete) | — |
| [RE Primer](reverse/re-primer.md) | Run provided C source | `moectf{r3v3rs3_1s_a_long_long_way_to_explore}` |
| [d0tN3t](reverse/dotnet.md) | .NET decompilation (dnSpy) | `moectf{7ce581d2-…}` |
| [Xor](reverse/xor.md) | Single-byte XOR | `moectf{e82b478d-…}` |
| [upx](reverse/upx.md) | UPX unpacking | `moectf{ec5390dd-…}` |
| [rc4](reverse/rc4.md) | RC4 + string cross-references | `moectf{why_Rc4_haS_…}` |
| [upx-revenge](reverse/upx-revenge.md) | Corrupted UPX header | `moectf{554ea35c-…}` |
| [TEA](reverse/tea.md) | TEA-family cipher (incomplete) | — |

Full flags are written at the top of each page.

## Coverage

- 27 challenges are documented.
- `ez_usbpcap` appears in the original notes as a title only, with no content, and is therefore omitted.
- Four entries are marked incomplete: `moejail_lv2`, `dynamic`, and `TEA` stop at the reconnaissance stage, and no flag was recorded. They are included for completeness rather than as solution references.

## Categories at a glance

- **Misc** — audio, image/document steganography, forensics, encoding, OSINT, Python jails
- **Web** — instance access and client-side interaction
- **Pwn** — remote service connectivity
- **Reverse** — .NET, XOR, packers, RC4, TEA

## License

The text is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
