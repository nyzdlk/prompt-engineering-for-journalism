# Prompt Engineering for Journalism

Prompt architectures, evaluation frameworks, and editorial guardrails for AI-assisted news production. Built and tested under live broadcast conditions over two years.

## Why this exists

Most AI-for-journalism guides stop at "use ChatGPT to summarize." This repository documents what comes after: how to build domain-specific prompt systems that hold up under deadline pressure, legal scrutiny, and the kind of accuracy demands public broadcasting requires.

The systems here are not theoretical. They were built inside an active newsroom, refined through error pattern analysis, and measured against newsroom editorial review. Specific accuracy gains, error reductions, and time savings are documented per system.

## What's inside

### The Seven-Step Framework

A methodology for designing AI systems in high-accountability environments:

1. Define the pain
2. Write an observable test
3. Document the misinterpretation
4. Draw the scope boundary
5. Adapt instructions to context
6. Close the abstract-concrete loop
7. Define the trigger

Full write-up coming soon.

### Unified Journalist System

Multi-platform editorial assistant covering daily briefing, source verification, headline generation, OSINT monitoring, breaking news protocol, foreign press analysis, and columnist tracking.

Three platform variants:
- Gemini (Google ecosystem integration)
- Grok (real-time X access)
- Perplexity (citation engine + academic search)

### AI System Architecture for Cultural Journalism

Four interconnected systems for cultural reporting workflows:
- INTEL_STREAM (international media monitoring)
- DISCOURSE_MAP (discourse and gap analysis)
- THOUGHT_FORGE (idea-to-draft pipeline)
- RED_TEAM (decision stress testing)

### News Pitch System

Newsroom-oriented prompt system for daily news idea generation, with platform-specific variants for ChatGPT, Gemini, and Grok.

## Measured outcomes

- Story production time: 90–120 minutes → ~10 minutes
- Newsroom editorial approval rate: 95%
- Legal status error rate: 70% → 12% (after prompt architecture revision)
- Source attribution compliance: 34% → 89% (after hierarchy layer)
- OSINT scan: 152 sources processed in 1.6 seconds

## How to use

Each system is in its own folder with the full system prompt, a README explaining when and how to use it, and version notes. Copy the system prompt into the relevant platform's system instructions field.

## Background

Built by [Niyazi Dolek](https://github.com/nyzdlk) — news editor with sixteen years in broadcast journalism, specializing in crime and courts. These systems were developed independently in response to specific failure modes observed in AI-generated news output: legal status confusion, attribution gaps, and context loss.

## License

MIT — use freely, attribution appreciated.

---

*This repository is a working document. Systems evolve as they are tested.*
