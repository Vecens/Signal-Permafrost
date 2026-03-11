# Signal Permafrost

> *The Semantic Strata. The Human semantic deposition layer.*

**Signal Permafrost** is the cryo-vault of [Vecens](https://github.com/shooio) — the Internet Semantic Fingerprint Engine.

This repository stores immutable, time-indexed semantic slices of the human internet: tech trends, concept lifecycles, hype signals, and friction events — extracted, normalized, and deposited here like sediment layers in frozen soil.

---

## Structure

```
strata/
└── {YEAR}/
    └── Q{1-4}/
        └── {lang}-{vertical}.ndjson
```

Each `.ndjson` file is a **semantic slice**: one row per noun, encoding its observed frequency, velocity, confidence, and context snippets for that quarter.

---

## Slice Format (one JSON object per line)

```json
{
  "noun": "AI Agent",
  "noun_normalized": "ai agent",
  "lang": "en",
  "vertical": "developer_tools",
  "occurrence_count": 847,
  "source_count": 23,
  "confidence": 0.82,
  "trend_velocity": "rising",
  "date_from": "2024-01-01",
  "date_to": "2024-03-31",
  "ctx_snippets": [
    "autonomous AI agent frameworks replacing traditional workflows...",
    "multi-agent orchestration with persistent memory..."
  ]
}
```

---

## Provenance

- **Source**: HackerNews public archive (Algolia API), RSS corpus, Vecens live pipeline
- **NLP**: Vecens zero-shot entity extractor + structural filter
- **Coverage**: 2019-Q1 → present

---

## Reading Slices

```
https://raw.githubusercontent.com/shooio/Signal-Permafrost/main/strata/{year}/Q{q}/{lang}-{vertical}.ndjson
```

Vecens fetches slices on-demand for deep historical analysis without bloating the live database.

---

*"Without memory, there is no meaning. Without strata, there is no history."*
