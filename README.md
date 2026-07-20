# FUCKYOU_DEREK — The Evidence Locker

> He said: *"go make art."* This is the art.

This repository is a **structured, searchable database** of the Derek & Merry situation, built for two purposes:

1. **The website** — laying it ALL out, module by module, with receipts.
2. **AI ingestion (Google AI Studio etc.)** — every file is chunked, indexed, and cross-referenced so an AI can pull exactly the piece it needs without choking on raw logs.

---

## How This Repo Is Organized

```
/
├── README.md                      ← you are here
├── 00_MASTER_INDEX.yaml           ← master map: every file, every module, every ID range
├── 00_ARCHITECTURE.md             ← the 7-module structure + 3-phase build plan
├── TIMELINE.md                    ← master chronology, Jan 2025 → May 2026
│
├── modules/                       ← THE MEAT. One file per module.
│   ├── MODULE_01_PROMISES.md      ← The Hook & The Bait
│   ├── MODULE_02_WITHHOLDING.md   ← The Control Mechanism
│   ├── MODULE_03_RUG_PULLS.md     ← The Neurological Trigger
│   ├── MODULE_04_GASLIGHTING_DARVO.md ← The Reality Rewrite
│   ├── MODULE_05_TRIANGULATION.md ← The Jay Hierarchy
│   ├── MODULE_06_EXPLOITATION.md  ← Emotional & Sexual Labor
│   └── MODULE_07_ERASURE.md       ← The Final Betrayal
│
├── evidence/
│   ├── whatsapp/
│   │   ├── chat_index_*.csv         ← EVERY message: ID, timestamp, speaker, text. Search by keyword.
│   │   ├── log_2025-11.md         ← monthly chunks, every message has a permanent WA-#### ID
│   │   ├── log_2025-12_part1.md   ← December split in 3 (biggest month): Dec 5–9
│   │   ├── log_2025-12_part2.md   ← Dec 9–14, incl. the Dec 12 confrontation
│   │   ├── log_2025-12_part3.md   ← Dec 18–31, incl. WA-1135 (the 1-hr video call)
│   │   ├── log_2026-01.md
│   │   ├── log_2026-02.md
│   │   ├── log_2026-05.md         ← the "reunion" logs (May 16–18, 2026)
│   │   └── SOURCE_ARTIFACTS.md    ← known source-export glitches, documented
│   ├── screenshots/
│   │   └── DEREK6_SCREENSHOT_INDEX.md  ← 28-page screenshot dossier, indexed & transcribed
│   └── transcripts/
│       └── VOICENOTE_DEREK1.md    ← voice note transcription
│
└── reports/                       ← third-party AI forensic analyses (verbatim)
    ├── FORENSIC_AUDIT_DOSSIER.md
    ├── FORENSIC_PATTERN_ANALYSIS.md
    └── HONESTY_VS_SINCERITY.md
```

## The ID System (how cross-referencing works)

- Every WhatsApp message has a permanent ID: **`WA-0001` … `WA-2105`**
- Modules cite evidence like this: `[WA-0560 · 12/12/25 9:09 AM]`
- To find any quote: search `chat_index_*.csv` by keyword → get the WA-ID → open the monthly log → read it in full context.
- Screenshot pages are **`SC-01` … `SC-28`** (source: `Derek6.pdf`).

## For AI Studio (how to pull in chunks)

Pull in this order — each is self-contained:

1. `00_MASTER_INDEX.yaml` + `00_ARCHITECTURE.md` (the map)
2. `TIMELINE.md` (the spine)
3. One `modules/*.md` at a time (the narrative + cited evidence)
4. `evidence/whatsapp/log_YYYY-MM.md` only when full message context is needed
5. `reports/*.md` for the third-party audits
6. `evidence/screenshots/DEREK6_SCREENSHOT_INDEX.md` for visual receipts

## Evidence Status & Known Gaps (read this before citing anything)

- **The first ~10 months are missing.** Contact began **Jan 26, 2025** (StarMaker). The exported WhatsApp log begins **Nov 5, 2025**. Everything before that survives only as **user testimony** and the third-party reports that analyzed it. Modules mark every claim as either `whatsapp_log` (hard receipt), `screenshot` (hard receipt), `user_testimony` (sworn account, not independently verifiable), or `report` (third-party AI analysis of testimony).
- **The WhatsApp export and the screenshots agree.** The 28 screenshot pages (Dec 12, 2025 fight) match the exported log line-for-line, timestamp-for-timestamp. The export has not been doctored in the overlapping region.
- **This is one side's archive.** It is organized to be *checkable*, not just *persuasive*. Every narrative claim points at a timestamped receipt you can read yourself.
- Names/handles: Merry = the archivist. Derek Vasilakis = the subject. "Jay" appears only via testimony (no logs). StarMaker activity referenced via testimony + reports.

## Message Statistics (from `chat_index_*.csv`)

| Metric | Value |
|---|---|
| Total messages (export) | 2,105 |
| From Merry | 1,726 (82.0%) |
| From Derek | 379 (18.0%) |
| Span of export | Nov 5, 2025 – Feb 16, 2026 + May 16–18, 2026 |
| Days in main span | 104 (Nov 5 – Feb 16) |
| Days Derek sent anything | 38 |
| Derek silence rate | ~63% of days, zero messages |

The asymmetry is not an interpretation. It is arithmetic.
