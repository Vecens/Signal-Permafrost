# 🧊 Signal Permafrost

> *"In the noise of the open web, we bury the signal."*
> —— The Semantic Strata Protocol

You have stumbled upon the **Cryo-Vault** of [Vecens](https://github.com/shooio), a high-frequency semantic radar scanning the human internet.

To the untrained eye, this repository is a wasteland of jagged JSON arrays and contextless timestamps. To an algorithmic operative, this is the most pristine, de-weaponized intelligence payload on the planet.

---

## 📁 The Strata Architecture (Blind-Core Storage)

We do not store articles. We do not store opinions. We store **Vectors of Hype and Friction**.

As the internet breathes, concepts are born, they mutate, and they decay. Vecens extracts these thermodynamic changes, strips them of their superficial UI, and freezes the raw semantic coordinates into `.ndjson` strata blocks. 

```text
strata/
└── {YEAR}/
    └── Q{1-4}/
        └── {lang}-{vertical}.ndjson
```

Anatomy of a Slice Every line you see is a frozen cross-section of a digital heartbeat.

Status: The radar is spinning. The permafrost is expanding.

"Without memory, there is no meaning. Without strata, there is no history."


---

## 🌐 CDN Access

All slices are readable without authentication via jsDelivr or raw GitHub:

```bash
# Raw GitHub
curl https://raw.githubusercontent.com/shooio/Signal-Permafrost/main/strata/2020/Q1/en-health_wellness.ndjson

# jsDelivr CDN (cached, faster)
curl https://cdn.jsdelivr.net/gh/shooio/Signal-Permafrost@main/strata/2020/Q1/en-ai_ml.ndjson
```

---

## 🗺️ Coverage

> Coverage table is updated automatically by the Vecens harvest pipeline.
> Each cell = number of noun slices preserved for that quarter.

| Year | Q1 | Q2 | Q3 | Q4 |
|------|----|----|----|----|
| 2019 | ✅ | 🔄 | 🔄 | 🔄 |
| 2020 | 🔄 | 🔄 | 🔄 | 🔄 |
| 2021 | 🔄 | 🔄 | 🔄 | 🔄 |
| 2022 | 🔄 | 🔄 | 🔄 | 🔄 |
| 2023 | 🔄 | 🔄 | 🔄 | 🔄 |
| 2024 | 🔄 | 🔄 | 🔄 | 🔄 |
| 2025 | 🔄 | 🔄 | 🔄 | 🔄 |

`✅ = deposited` · `🔄 = pending` · `—= not applicable`

---

## ⚙️ Integration with Vecens

The live Vecens engine queries this vault on-demand for historical context:

```typescript
import { fetchFromVault, traceNounInVault } from '@/lib/vault/fetch-vault'

// Fetch all nouns for a specific period + vertical
const aiSlice = await fetchFromVault(2020, 1, 'en', 'ai_ml')

// Trace a noun's semantic trajectory across all preserved quarters
const trajectory = await traceNounInVault('transformer')
// → [{ year: 2019, q: 1, occurrenceCount: 3, avgHype: 0.4 }, ...]
```

---

## 📜 Provenance

- **Source corpus:** Hacker News via [Algolia HN Search API](https://hn.algolia.com/api) (CC0 public domain)
- **Extraction engine:** [Vecens](https://github.com/shooio) — proprietary NLP pipeline
- **Deposit cadence:** Quarterly, automated via `npm run vault:harvest`
- **License:** CC0 1.0 Universal — Public Domain Dedication

---

## 🔒 What This Is Not

- ❌ Not a news archive — no full articles, no URLs stored
- ❌ Not an opinion database — no sentiment labels, no political tagging
- ❌ Not personally identifiable — no authors, no usernames, no links
- ✅ Pure semantic frequency distribution — the shape of collective attention, nothing more

---

> *"Without memory, there is no meaning. Without strata, there is no history."*

**Status:** 🟢 The radar is spinning. The permafrost is expanding.
