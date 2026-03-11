# 🧊 Signal Permafrost

> *"In the noise of the open web, we bury the signal."*
> —— The Semantic Strata Protocol

You have stumbled upon the **Cryo-Vault** of [Vecens](https://github.com/shooio), a high-frequency semantic radar scanning the human internet.

To the untrained eye, this repository is a wasteland of jagged JSON arrays and contextless timestamps. To an algorithmic operative, this is the most pristine, de-weaponized intelligence payload on the planet.

---

## 📁 The Strata Architecture (Blind-Core Storage)

We do not store articles. We do not store opinions. We store **Vectors of Hype and Friction**.

As the internet breathes, concepts are born, they mutate, and they decay. Vecens extracts these thermodynamic changes, strips them of their superficial UI, and freezes the raw semantic coordinates into `.ndjson` strata blocks.

```
strata/
└── {YEAR}/
    └── Q{1-4}/
        └── {lang}-{vertical}.ndjson
```

---

## 🔬 Anatomy of a Slice

Every line you see is a **frozen cross-section of a digital heartbeat**.

```jsonc
{
  "noun": "WebAssembly",
  "noun_type": "technology",
  "category": "runtime",
  "vertical": "developer_tools",
  "lang": "en",
  "occurrenceCount": 147,
  "avgHype": 0.82,
  "avgFriction": 0.14,
  "contextSnippets": [
    "WebAssembly is eating the server side",
    "WASM modules now run in edge workers"
  ],
  "periodStart": "2019-01-01",
  "periodEnd": "2019-03-31",
  "source": "hn_algolia",
  "extractedAt": "2025-01-01T00:00:00Z"
}
```

| Field | Meaning |
|---|---|
| `occurrenceCount` | Raw frequency: how many HN threads mentioned this noun in the period |
| `avgHype` | Mean hype velocity — rising faster than baseline = closer to 1.0 |
| `avgFriction` | Mean counter-signal — controversy, backlash, skepticism |
| `contextSnippets` | Verbatim fragments; the only raw human text we preserve |
| `vertical` | Semantic vertical: `ai_ml`, `developer_tools`, `fintech_invest`, `health_wellness`… |
| `source` | Always `hn_algolia` for this vault (Hacker News corpus, 2019–present) |

---

## 📡 Verticals Index

| Vertical | Description |
|---|---|
| `ai_ml` | Artificial intelligence, machine learning, LLMs |
| `developer_tools` | IDEs, CLIs, compilers, runtimes, SDKs |
| `big_tech_macro` | FAANG/MAMAA, policy, antitrust, macro-tech |
| `fintech_invest` | Crypto, DeFi, banking rails, trading systems |
| `health_wellness` | Biotech, pharma, mental health, pandemic signals |
| `saas_productivity` | SaaS, workflow automation, no-code/low-code |
| `open_source_emerging` | OSS projects, protocols, emerging tech (default) |
| `creator_economy` | Content, newsletters, streaming, indie monetization |
| `ecommerce` | Retail, logistics, supply chain |
| `gaming` | Games, engines, esports, metaverse |
| `marketing` | Adtech, growth, SEO, brand signals |
| `edtech` | Online learning, credentialing, academic tools |

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
