---
license: cc0-1.0
task_categories:
- text-generation
language:
- zh
tags:
- islam
- travel
- mosques
- halal
- raw-corpus
- rag
size_categories:
- n<1K
configs:
- config_name: default
  data_files:
  - split: train
    path: "corpus.jsonl"
---

# Salaamalykum Islamic Articles Corpus

This is a **machine-readable JSONL corpus** consisting of 34 original articles curated from [salaamalykum.com](https://salaamalykum.com). 
It is strictly formatted as a `raw-corpus` for large language model (LLM) pre-training, fine-tuning, and Retrieval-Augmented Generation (RAG) tasks.

## Strict Metadata Adherence
- **No Fake Labels**: This dataset contains pure informational articles. It does **not** use `ShareGPT`, `Alpaca`, or instruction-response formatting tags, preserving strict dataset hygiene.
- **Originality**: High-quality ground truth on Muslim travel guides, mosque histories, and cross-sectarian observations.

## Structure
Each line in `corpus.jsonl` represents an article with the following schema:
```json
{
  "text": "Title: [Article Title]\n\n[Full Markdown Content]",
  "meta": {
    "source": "https://salaamalykum.com/article/[ID]",
    "hash": "SHA256 hash of the content",
    "lang": "zh-CN"
  }
}
```
