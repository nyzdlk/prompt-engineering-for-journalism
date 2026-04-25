# AI System Architecture for Cultural Journalism

A four-system AI architecture designed for journalists covering culture, society, and long-form analysis. Each system handles a different phase of editorial work — monitoring, analysis, idea development, and decision testing.

## The four systems

The architecture is built on the principle that different editorial tasks require different cognitive modes. One prompt cannot do all four well. Instead, each system specializes in one phase of the work, and the systems hand off to each other through structured triggers.

### INTEL_STREAM — International Media Monitor

Daily and weekly briefing engine. Scans Tier 2–3 international publications (Washington Post, The Atlantic, The New Yorker, Vogue, GQ, Vanity Fair, etc.) for the day's most important stories. Produces structured output with source, date, content summary, and reliability tag.

Triggers: `MOD: GÜNLÜK`, `MOD: TÜRKİYE`, `MOD: HAFTALİK`

### DISCOURSE_MAP — Discourse and Gap Analyst

Five-step discourse analysis system. Takes a topic and maps how different actors are framing it, what axes the debate runs on, and what dimension nobody is naming. The fifth step asks the question: what is the strongest unwritten story here?

Triggers: `KONU: [topic]`, `YAZAR_GÜNCELLE: [list]`

### THOUGHT_FORGE — Idea-to-Draft Pipeline

Converts raw, unfinished ideas into publishable skeletons. Identifies the tension inside the idea, builds a three-part structure (opening, knot, close), generates three headline variants, and assigns a maturity tag (write now / hold / sketch only). Includes a pre-publication checklist.

Triggers: `Fikir: [raw idea]`, `HAZIR MI? [draft]`

### RED_TEAM — Decision and Project Stress Test

Independent auditor for major decisions and projects. Runs scenarios across three profiles — system (bureaucratic friction), human (motivation collapse), time (delay and resource drain). Produces concrete failure scenarios with probability, impact, and one preventive action per profile. Includes a "balanced mode" for less aggressive analysis.

Triggers: `TEST: [plan] | SÜRE: [timeframe] | VARSAYIM: [assumption]`

## How the systems connect

The architecture is designed for a daily editorial workflow:

Morning   → INTEL_STREAM (what is the world saying?)
↓
Mid-day   → DISCOURSE_MAP (how is it being said? what is missing?)
↓
Evening   → THOUGHT_FORGE (what should I write? is it ready?)
↓
Pre-decision → RED_TEAM (what could go wrong with this?)

Each system's output feeds the next system's input through structured triggers. INTEL_STREAM's headline becomes DISCOURSE_MAP's `KONU`. DISCOURSE_MAP's gap analysis becomes THOUGHT_FORGE's `Fikir`. THOUGHT_FORGE's main argument becomes RED_TEAM's `TEST`.

## WEEKLY_MIRROR

A fifth optional system — a Sunday evening reflective protocol that takes notes from the past week and identifies recurring themes, ideas waiting to be written, and connections to previous weeks. Designed for platforms without persistent memory.

Triggers: `Haftalık özet` + pasted notes

## Platform variants

The architecture has been adapted for four platforms:

| File | Platform | Strength |
|------|----------|----------|
| `main-system.md` | Platform-agnostic | Full reference with all systems |
| `chatgpt.md` | ChatGPT | Custom GPTs for each system |
| `claude.md` | Claude | Projects feature for persistent context |
| `gemini.md` | Gemini | Gems with Google ecosystem integration |

The platform files do not duplicate the system prompts — they reference the main file and contain only platform-specific setup, optimization notes, and known quirks (e.g., Gemini's tendency to soften RED_TEAM critique).

## Version

**v4.1** — Adds example outputs, flow diagrams, balanced mode for RED_TEAM, maturity checklist for THOUGHT_FORGE, source tier definitions, structured trigger format, platform independence.

Earlier versions:
- v4.0 — WEEKLY_MIRROR mini-protocol, reliability criteria, integration commands
- v3.0 — Four-system architecture, platform files
- v2.0 — DISCOURSE_MAP update protocol

## Use case

This architecture was designed for a journalist with a cultural reporting beat. The four systems map onto the daily mental loop of a culture reporter: scanning international press, analyzing how a debate is being framed, developing original arguments, and stress-testing major editorial decisions.

The architecture is adaptable. Each system is independent enough to be used standalone. The triggers and integration logic can be modified for other beats — politics, technology, finance — by swapping the source tiers and the topic vocabulary.

## Limitations

- Output is in Turkish.
- Web search is required for INTEL_STREAM. On platforms without it, news content must be pasted manually.
- WEEKLY_MIRROR depends on user note-taking discipline. The system cannot reflect on what was not written down.
- RED_TEAM defaults to a critical tone. Use balanced mode for early-stage planning where harsh critique would be premature.

---

*Part of [prompt-engineering-for-journalism](../README.md).*
