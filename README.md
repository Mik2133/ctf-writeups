# CTF Writeups

Writeups for CTF challenges I have solved, written in English.

I document each challenge as I work through it — the approach, the dead ends, and the final solution. The notes were originally kept in Chinese; this repository is the English version, maintained for reference and for sharing with the wider security community.

## Events

| Event | Categories | Writeups |
|---|---|---|
| [MoeCTF 2024](moectf-2024/README.md) | Misc, Web, Pwn, Reverse | 27 |

## Structure

```
<event>/
  README.md          index for the event
  misc/              one Markdown file per challenge
  web/
  pwn/
  reverse/
  assets/<slug>/     screenshots used by that challenge's writeup
```

Each writeup follows the same layout: a metadata table with the category and the flag, the challenge description, the solution with annotated screenshots, and a short list of takeaways.

## Conventions

- Flags are quoted verbatim, including any `moectf{...}`-style wrapper.
- Commands and payloads are shown as they were run, not normalised after the fact.
- Challenges that were not finished are marked as incomplete rather than presented as solved.
- Writeups that were translated from Chinese keep their original screenshots.

## License

The text of these writeups is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
