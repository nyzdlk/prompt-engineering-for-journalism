# Editorial Rule System

A rule system for writing and auditing TV news with AI. It is my current work.

## What it is

- **One master rule file.** A script turns it into three profiles: story writing, wall graphics (Wall) and audit.
- **36 red lines.** The rules that real tests broke most often, each one line long. Every story is checked against them before delivery.
- **77 mechanical checks for stories, 11 for Wall.** A script measures everything that can be counted: line lengths, tags, sentence counts, banned phrases.
- **47 gold-standard example stories** (*altın numune*). Each one shows the expected output for one story type.
- **Platforms:** Claude, ChatGPT, Gemini.

## How it changes

The rule, the examples and the script are always updated together. A rule that the script cannot measure, or that no example shows, is not finished.

Revision cycle:

test → finding → rule → example → script → test

## Files in this folder

- [red-lines.md](red-lines.md): selected red lines, each with a wrong and a right version from a real case
- [checks.md](checks.md): sample check codes and what they measure
- [testing.md](testing.md): how every rule change is tested
- [examples/](examples/): three anonymised cases, before and after

The master rule file and the script are not published in this repository; this folder documents the rules, the checks and the test method.

## Terms

The system works in Turkish. A few newsroom terms appear in these pages:

| Term | Meaning |
|---|---|
| KAM | Anchor intro read on camera |
| METİN / gövde | Story body read over pictures |
| SES | Soundbite of a named speaker |
| RÖP | Street interview (vox pop) |
| ANONS | Reporter's piece to camera |
| KUŞAK | On-screen text band, read by viewers with the sound off |
| KJ | Name and title caption |
| Wall | Studio wall graphic |
| FAIL / UYARI | Script result: fail / warning |
