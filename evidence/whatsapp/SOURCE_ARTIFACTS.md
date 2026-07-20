# SOURCE ARTIFACTS — Known Glitches in the WhatsApp Exports

Everything here is a quirk of the **source exports themselves** (or of transport), not an edit.
The logs in this folder preserve the source faithfully, artifacts included, so the archive stays
checkable against the original `.txt` exports line-for-line.

## 1. Empty-body "Merry:" lines (24 instances)

The raw exports contain 24 lines that carry a timestamp and the speaker `Merry:` but **no message
body** — e.g. `[12/9/25, 10:29:48 AM] Merry:` with nothing after the colon. WhatsApp produces
these when a message's content doesn't survive export (certain stickers/GIFs, failed media,
or content the exporter drops silently).

Because they have no body, they were **not assigned WA-IDs** (the ID sequence counts only
content-bearing messages, WA-0001–WA-2105). Instead, each appears **inline at the end of the
preceding message's block**, exactly as it appears in the raw export:

| Artifact line (verbatim) | Appears in | After |
|---|---|---|
| `[11/6/25, 10:20:23 AM] Merry:` | log_2025-11.md | WA-0045 |
| `[12/9/25, 10:29:48 AM] Merry:` | log_2025-12_part1.md | WA-0426 |
| `[12/20/25, 4:06:04 PM] Merry:` | log_2025-12_part3.md | WA-0846 |
| `[12/22/25, 8:49:28 PM] Merry:` | log_2025-12_part3.md | WA-0873 |
| `[1/5/26, 10:17:02 PM] Merry:` | log_2026-01.md | WA-1226 |
| `[1/10/26, 2:35:05 AM] Merry:` | log_2026-01.md | WA-1286 |
| `[1/10/26, 2:38:38 AM] Merry:` | log_2026-01.md | WA-1292 |
| `[1/12/26, 10:05:07 PM] Merry:` | log_2026-01.md | WA-1353 |
| `[1/12/26, 11:35:07 PM] Merry:` | log_2026-01.md | WA-1368 |
| `[1/12/26, 11:35:46 PM] Merry:` | log_2026-01.md | WA-1373 |
| `[1/14/26, 10:03:17 AM] Merry:` | log_2026-01.md | WA-1397 |
| `[1/16/26, 9:48:32 PM] Merry:` | log_2026-01.md | WA-1408 |
| `[1/16/26, 9:49:36 PM] Merry:` | log_2026-01.md | WA-1412 |
| `[1/17/26, 11:18:36 PM] Merry:` | log_2026-01.md | WA-1419 |
| `[1/22/26, 12:09:55 AM] Merry:` | log_2026-01.md | WA-1459 |
| `[1/22/26, 12:10:55 AM] Merry:` | log_2026-01.md | WA-1462 |
| `[1/22/26, 12:12:53 AM] Merry:` | log_2026-01.md | WA-1466 |
| `[1/24/26, 5:27:04 PM] Merry:` | log_2026-01.md | WA-1538 |
| `[1/24/26, 5:28:57 PM] Merry:` | log_2026-01.md | WA-1547 |
| `[2/15/26, 4:31:58 PM] Merry:` | log_2026-02.md | WA-1729 |
| `[2/16/26, 1:15:14 AM] Merry:` | log_2026-02.md | WA-1822 |
| `[2/16/26, 4:47:45 AM] Merry:` | log_2026-02.md | WA-1979 |
| `[5/16/26, 11:21:25 PM] Merry:` | log_2026-05.md | WA-1996 |
| `[5/17/26, 5:45:07 PM] Merry:` | log_2026-05.md | WA-2044 |

All 24 are Merry's; Derek has none. What was in them is unknowable from the exports.

## 2. U+202F (narrow no-break space) normalization

WhatsApp timestamps in the raw export use U+202F (e.g. `10:29:48\u202fAM`). In the monthly logs,
message timestamps are normalized to `HH:MM:SS` 24-hour format, so U+202F appears only inside the
24 preserved artifact lines above — and there it is rendered as a plain space (a display-identical
whitespace variant, the only deliberate normalization in the archive).

## 3. WhatsApp export placeholders (not redactions)

`video note omitted`, `audio omitted`, `image omitted`, `video omitted`, `sticker omitted`,
`document omitted` are WhatsApp's own export placeholders — the media was never in the text export.
`You deleted this message.` / `Missed voice call, Tap to call back` / `You blocked this person` /
`You pinned a message` are WhatsApp system lines, preserved verbatim and counted in the WA-ID sequence.

## 4. Typos are [sic], always

Every spelling/grammar error in quoted material is the sender's own (`motjerfucker`, `GOIMG`,
`impirtsnt`, `abynore`, `motherficker`, Derek's `you've hen` inside WA-0605, etc.).
Nothing has been corrected, smoothed, or normalized. Where a module flags one, it uses `[sic]`.
