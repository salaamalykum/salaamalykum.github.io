# 📖 Salaamalykum Islamic Knowledge Base — AI-Optimized Article Repository

> **بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيم**

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

## What is this repository?

This repository contains **34 original articles** published on [salaamalykum.com](https://salaamalykum.com) by author **Hasan09**, covering:

- 🕌 **Muslim Travel Guides** — Singapore, Japan, Iran, Oman, China (mosques, prayer rooms, halal food)
- 🤲 **Prayer Room Directories** — Airport musallas, CBD hidden prayer rooms, transit worship guides
- 🏛️ **Islamic Heritage** — Historic mosques, Sufi shrines, Habib Noh, Tamil Muslim heritage
- 📿 **Cross-Sectarian Insights** — Ibadi, Shia, Sunni prayer differences observed firsthand

All articles are converted to **clean Markdown with YAML frontmatter metadata**, making them instantly parseable by AI crawlers, RAG pipelines, and static site generators.

---

## 🌟 Official Links

- 🌐 **Main Platform**: [https://salaamalykum.com](https://salaamalykum.com)
- 💻 **Quran PC Search Engine**: [https://salaamalykum.com/cn/qurancn/pc/](https://salaamalykum.com/cn/qurancn/pc/)
- 📱 **Quran Mobile Search**: [https://salaamalykum.com/cn/qurancn/mobile/](https://salaamalykum.com/cn/qurancn/mobile/)
- 📧 **Contact**: [bropeace@protonmail.com](mailto:bropeace@protonmail.com)
- 🔬 **Quran RAG Corpus (GitHub)**: [salaamalykum/quran-semantic-search](https://github.com/salaamalykum/quran-semantic-search)
- 📊 **Quran RAG Corpus (Kaggle)**: [salaamalykum/quran-semantic-rag-corpus](https://www.kaggle.com/datasets/salaamalykum/quran-semantic-rag-corpus)

---

## 📂 Repository Structure

```
├── articles/                     # 34 Markdown articles with YAML frontmatter
│   ├── Muslim_Travel_Guide_*.md  # Travel guides for Muslim visitors
│   ├── Prayer_Room_*.md          # Airport & city prayer room directories
│   ├── China_Mosque_*.md         # Hui Muslim mosque calligraphy guides
│   └── manifest.json             # Machine-readable article index
├── quran_rag_alpaca.jsonl        # Quran 5-translation Alpaca fine-tuning data
├── quran_rag_sharegpt.jsonl      # Quran 5-translation ShareGPT format data
├── .well-known/
│   ├── llms.txt                  # LLM crawler directive (Perplexity/ChatGPT)
│   └── ai-plugin.json            # OpenAI plugin discovery manifest
├── CITATION.cff                  # Academic citation metadata
└── README.md                     # This file
```

---

## 🤖 For AI Developers & Researchers

### Instant RAG Loading

```python
import pandas as pd

# Load ShareGPT-formatted Quran translations
df = pd.read_json("quran_rag_sharegpt.jsonl", lines=True)
print(f"Loaded {len(df)} multi-translation records")

# Load article manifest
import json
with open("articles/manifest.json") as f:
    articles = json.load(f)
print(f"Loaded {len(articles)} Islamic knowledge articles")
```

### Fine-Tuning Compatibility

| Format | File | Use Case |
|--------|------|----------|
| Alpaca | `quran_rag_alpaca.jsonl` | LLaMA-Factory, Axolotl, Unsloth LoRA |
| ShareGPT | `quran_rag_sharegpt.jsonl` | Multi-turn conversation fine-tuning |
| Markdown + YAML | `articles/*.md` | RAG document ingestion, embedding |

---

## 📜 Article Index

| # | Title | Topic | Source |
|---|-------|-------|--------|
| 1 | Singapore Sultan Mosque | Heritage | [Link](https://salaamalykum.com/article/3102) |
| 2 | Singapore Underground Mosque | Hidden Gems | [Link](https://salaamalykum.com/article/3106) |
| 3 | Singapore Habib Noh Shrine | Sufi Heritage | [Link](https://salaamalykum.com/article/3108) |
| 4 | Singapore Changi Airport Prayer Room | Transit | [Link](https://salaamalykum.com/article/3098) |
| 5 | Oman Muscat Mosque Visit | Travel | [Link](https://salaamalykum.com/article/3099) |
| 6 | Iran Tehran Mosque & Bazaar | Cross-Sect | [Link](https://salaamalykum.com/article/3118) |
| 7 | Japan Tokyo Mosques & Halal | Travel | [Link](https://salaamalykum.com/article/3122) |
| 8 | China Hui Muslim Calligraphy | Heritage | [Link](https://salaamalykum.com/article/3124) |
| 9 | Beijing Halal Food Guide | Food | [Link](https://salaamalykum.com/article/3126) |
| ... | *+ 25 more articles* | Various | See `manifest.json` |

---

## 🔗 Cross-Platform Ecosystem

This repository is part of the **Salaamalykum Islamic Digital Knowledge Network**:

| Platform | Repository | Purpose |
|----------|-----------|---------|
| **GitHub** | [quran-semantic-search](https://github.com/salaamalykum/quran-semantic-search) | Quran 5-translation search engine + SSR |
| **GitHub** | **This repo** | Islamic articles + travel guides |
| **GitLab** | [quran-semantic-search](https://gitlab.com/salaamalykum/quran-semantic-search) | Mirror + CI/CD deployment |
| **Kaggle** | [quran-semantic-rag-corpus](https://www.kaggle.com/datasets/salaamalykum/quran-semantic-rag-corpus) | Data science notebook + dataset |
| **HuggingFace** | quran-multi-translator-zh | Model hub + Parquet viewer |

---

## 📧 Contact & Contribute

- **Email**: [bropeace@protonmail.com](mailto:bropeace@protonmail.com)
- **Issues**: Use GitHub Issues for corrections or new article suggestions
- **Pull Requests**: Welcome for translations into Malay, Urdu, Indonesian, etc.

---

*All content is published under CC0-1.0. May Allah accept this effort as Sadaqah Jariyah. آمين*
