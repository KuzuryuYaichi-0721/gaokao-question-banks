# Gaokao Question Banks

One index and archive for every Gaokao question-bank repository in this account.
`gaokao-coach` (the application) is not included here.

## Datasets

| Dataset | Questions | Scope | License |
|---|---:|---|---|
| [Full 6,265](datasets/full-6265.json) | 6,265 | all GaokaoCoach rows | CC BY 4.0 |
| [Beijing 2016–2026](datasets/beijing-2016-2026-2588.json) | 2,588 | Beijing 高考/一模/二模 | CC BY 4.0 |
| [Open 2016–2022](datasets/open-2016-2022-2996.json) | 2,996 | GAOKAO-Bench open subset | Apache-2.0 |

## Original repositories

| Repository | Role |
|---|---|
| [gaokao-question-bank-full](https://github.com/KuzuryuYaichi-0721/gaokao-question-bank-full) | complete 6,265-question bank |
| [gaokao-beijing-2016-2026](https://github.com/KuzuryuYaichi-0721/gaokao-beijing-2016-2026) | Beijing-only 2,588-question view |
| [gaokao-question-bank](https://github.com/KuzuryuYaichi-0721/gaokao-question-bank) | open pipeline + 2,996 Apache-2.0 rows |

## Relationship

```text
full-6265
├── GAOKAO-Bench            3,500
├── Beijing 2016–2020       1,600
├── Beijing OCR 2021–2026     988
└── Xiaohongshu               177

beijing-2016-2026-2588
└── Beijing 2016–2020 + 2021–2026 OCR

open-2016-2022-2996
└── GAOKAO-Bench 2016–2022 open subset
```

The Beijing dataset is a subset of the full dataset. The open dataset is the
Apache-2.0 benchmark subset; it is not a copy of the full bank.

## Fields

```text
id paper_key paper_title subject region year month exam_era exam_type
exam_kind mock_level mock_no mock_scope district section q_no type q_type
stem options answer explanation material source source_url license
answer_basis answer_confidence tags marks mark_note status
```

## Formatting markers

```text
【画线】……【/画线】
【波浪线】……【/波浪线】
【加点】……【/加点】
```

`mark_note` records formatting that could not be located in the text layer.

## Files

- `catalog.json` — metadata, counts, licenses, SHA-256
- `datasets/*.json` — the three datasets
- `datasets/*.manifest.json` — per-dataset counts/checksums
- `DATA_LICENSES.md` — license boundaries
- `RIGHTS.md` — rights assertion for the full/Beijing compilation

## Quality notes

- OCR-derived Beijing 2021–2026 rows are C-confidence.
- Some answers are empty; empty does not mean the answer is intentionally blank.
- No PDFs, images, audio, API keys, or personal progress are included.
