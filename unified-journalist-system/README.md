# Unified Journalist & News Editor System

Multi-platform editorial assistant for AI-assisted news production. Combines Reuters/BBC/AP journalism standards, Turkish Language Institute (TDK) writing rules, and Turkish media law into a single command-driven system.

## What it does

A working editorial assistant that handles:

- Daily briefing and news scanning (`sabah`, `tara`)
- Source verification with academic backing (`teyit`)
- Headline generation with SEO analysis (`başlık`)
- Pre-publication editorial review — 10-point checklist (`kontrol`)
- OSINT location-based monitoring (`osint`)
- Breaking news protocol with verification tiers (`breaking`, `breaking güncelle`)
- Foreign press comparative analysis (`gundem`)
- Columnist tracking and analysis (`köşe yazarı`)
- Real-time pulse measurement on X (`nabız` — Grok only)
- Visual content suggestions (`infografik` — Gemini only)

## Platform variants

The system has four files. Each one targets a different platform's strength:

| File | Platform | Strength |
|------|----------|----------|
| `unified.md` | Platform-agnostic | Full reference version |
| `gemini.md` | Google Gemini | Scholar, Trends, YouTube, Maps integration |
| `grok.md` | xAI Grok | Real-time X access, public sentiment |
| `perplexity.md` | Perplexity | Citation engine, academic search |

The platform-agnostic version (`unified.md`) is the canonical reference. The three platform variants adapt the same logic to each platform's specific capabilities.

## Version

**v9.0** — All files synchronized to a single version number. Earlier versions had drift between platforms (UNIFIED v8.0 + platform v4.0). v9.0 unifies the version line.

Key changes in v9.0:
- Single command: `teyit [iddia]` (replaced `dogrula`)
- Standardized labels: `[DOĞRULANAMADI]`, `[TEYİT BEKLENİYOR]`, `[WHITELIST DIŞI KAYNAK]`
- Reuters, AP, AFP, Bloomberg, AA promoted to Tier 1
- DHA, İHA moved to Tier 2
- Whitelist synchronized across all platforms
- OSINT scope explicitly defined (what is collected, what is not)
- KVKK and Law 5651 (Turkish internet law) coverage expanded
- `breaking` template now identical across all platforms
- `dosya güncelle` mechanism added for long-running investigations

Full changelog inside each file.

## How to use

1. Choose the platform you want to use (Gemini, Grok, Perplexity, or the platform-agnostic version).
2. Open a new conversation in that platform.
3. Paste the entire system file as the system prompt.
4. Use commands directly:

sabah
breaking deprem
teyit "Cumhurbaşkanı istifa etti"
başlık faiz kararı
analiz [URL] + kontrol
tara İBB 48s
gundem Türkiye seçim
nabız merkez bankası          ← Grok only
infografik [veri]             ← Gemini only

Each command's output template and behavior is defined inside the file.

## Limitations

- All output is in Turkish (an English version is planned).
- Real-time commands (`sabah`, `radar`, `sessiz kriz`, `fırsat`) require live data input on platforms without web search.
- `nabız` runs automatically only on Grok — other platforms require manual data paste.
- `köşe yazarı` requires URL or publication name to function.
- Output requires human editorial review before publication.

## Background

Built and tested under live broadcast conditions. The system evolved through iterative testing, error pattern analysis, and platform-specific adaptation. Earlier versions are documented in commit history.

---

*Part of [prompt-engineering-for-journalism](../README.md).*
