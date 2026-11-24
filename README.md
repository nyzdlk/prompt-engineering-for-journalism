# Prompt Engineering for Journalism

Prompt architectures, evaluation frameworks, and editorial guardrails for AI-assisted news production. Built and tested under live broadcast conditions since 2023.

## Why this exists

Most AI-for-journalism guides stop at "use ChatGPT to summarize." This repository documents what comes after: how to build domain-specific prompt systems that hold up under deadline pressure, legal scrutiny, and the kind of accuracy demands broadcast news requires.

The systems here are not theoretical. They were built inside an active newsroom, refined through error pattern analysis, and measured against newsroom editorial review.

## What's inside

### Editorial Rule System (current work)

A rule system for writing and auditing TV news with AI, used with Claude, ChatGPT and Gemini. One master rule file generates three profiles: story writing, wall graphics and audit. It has 36 red-line rules, a script with 77 mechanical checks for stories and 11 for wall graphics, 47 gold-standard example stories, and a test suite that every rule change must pass.

Full write-up: [Editorial Rule System](editorial-rule-system/README.md).

### The Seven-Step Framework

A methodology for designing AI systems in high-accountability environments:

1. Define the pain
2. Write an observable test
3. Document the misinterpretation
4. Draw the scope boundary
5. Adapt instructions to context
6. Close the abstract-concrete loop
7. Define the trigger

Full write-up: [The Seven-Step Framework](seven-step-framework/README.md).

### Unified Journalist System

Multi-platform editorial assistant covering daily briefing, source verification, headline generation, OSINT monitoring, breaking news protocol, foreign press analysis, and columnist tracking.

Three platform variants (reference; current work uses Claude and ChatGPT):
- Gemini (Google ecosystem integration)
- Grok (real-time X access)
- Perplexity (citation engine + academic search)

### AI System Architecture for Cultural Journalism

Four interconnected systems for cultural reporting workflows:
- INTEL_STREAM (international media monitoring)
- DISCOURSE_MAP (discourse and gap analysis)
- THOUGHT_FORGE (idea-to-draft pipeline)
- RED_TEAM (decision stress testing)

## Measured outcomes

*Based on my own tests, not peer-reviewed.*

- Copy desk approval time for my stories: 40 minutes → 3–4 minutes, with no or minimal edits
- Legal status error rate: 70% → 12% (after prompt architecture revision)
- Source attribution compliance: 34% → 89% (after hierarchy layer)

How this is measured: every story I write goes to the copy desk, which edits it and approves it for broadcast. I track how long approval takes and how much the desk changes.

## How to use

The Unified Journalist System folder contains the full system prompts; copy one into the relevant platform's system instructions field. The Seven-Step Framework and AI System Architecture folders contain write-ups only; their prompts are not published here. The Editorial Rule System folder documents the rules, the checks and the test method.

## Background

Built by [Niyazi Dölek](https://github.com/nyzdlk) — news editor in broadcast journalism since 2010, specializing in crime and courts. These systems were developed independently in response to specific failure modes observed in AI-generated news output: legal status confusion, attribution gaps, and context loss.

## License

MIT — use freely, attribution appreciated.

---

*This repository is a working document. Systems evolve as they are tested.*
