# FallSeed Recruitment Firm

> **A Progressive Web App (PWA) seed for UK Recruit firms.**
> One HTML file. Four base tools + LLM-agnostic build engine + Fork Seed packager. MIT. Sovereign.

**Live:** https://sjgant80-hub.github.io/fallseed-recruit/

## What this is

`fallseed-recruit` is a single HTML file you can save to your desktop or install as a PWA. It bundles:

- The four base tools of the Recruit wedge (anchor / onboard / paper / practice)
- A build engine that generates new tools on demand using any LLM (WebLLM in-browser, ollama / LM Studio local, Groq / OpenRouter free cloud, or BYOK paid)
- A Fork Seed packager that lets you mutate the seed for a different vertical or client

## Vertical context

Recruitment · employment agency · temp (UK).

## Base tools

| Role | Tool | Purpose |
|---|---|---|
| anchor | [`fallrecruit`](https://sjgant80-hub.github.io/fallrecruit/) | Candidate register · client register · vacancy tracker · placement records · AWR clock · IR35 SDS log · RTW evidence · 12-pt compliance |
| onboard | [`fallrecruitonboard`](https://sjgant80-hub.github.io/fallrecruitonboard/) | Candidate onboarding · RTW · DBS · references · skills · qualifications · privacy · opt-out (Reg 32) · pay & holiday agreement |
| paper | [`fallrecruitpaper`](https://sjgant80-hub.github.io/fallrecruitpaper/) | Reg 14 / 15 terms · Reg 32 opt-out · introduction fee terms · temp-to-perm transfer fees · KID · NDA · privacy notice |
| practice | [`fallrecruitpractice`](https://sjgant80-hub.github.io/fallrecruitpractice/) | Workflow · placement pipeline · AWR 12-week clock · KID delivery log · CPD · complaints · compliance file reviews |

## Architecture

- **One HTML file** — no build step, no server, no install
- **IDB primary** — every record lives in `IndexedDB` (`fallseed-recruit-v2`) on your device
- **BroadcastChannel mesh** — `fall-recruit` for cross-tool sync; `fall-signal` for global hello
- **Mansoor P3 audit chain** — `prevHash` + SHA-256 chained entries on every mutation
- **8-provider LLM cascade** — WebLLM (T1) → ollama / LM Studio (T2) → Groq / OpenRouter free / Google / Cerebras (T3-free) → Anthropic (T3-paid)
- **Streaming** — SSE token-by-token output
- **Fork Seed packager** — serialises a mutated SEED back into a new self-contained HTML

## Sovereignty

- MIT-licensed
- No telemetry, no analytics, no tracking
- All data stays on your device (IDB) — nothing posted unless you wire an external LLM
- Works offline once installed as PWA
- One-time payment; upgrades optional

## Cosmology

Prime **1187**, spine-clean mod 127. Mesh channel **`fall-recruit`**. Bundle roles **anchor / onboard / paper / practice**. Seal **◊·κ=1**.

Part of the FallSeed family — see [www.ai-nativesolutions.com](https://www.ai-nativesolutions.com).

## Licence

MIT © Simon Gant.
