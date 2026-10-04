# HF_Leaderboard_Lab_Results

**Project:** `K_RAVEN`  
**Tier:** `TIER_4_INFERENCE_AGENTS`  
**Slug:** `WeiyingZhao/Regularized-Recursive-Self-Improvement-of-Agent-Harnesses`  
**Commit:** `d5a84b8d0b44`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **48.21 ms** |
| Min latency | 43.49 ms |
| Max latency | 54.04 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **52** |
| Tokenization latency | 1.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5873 |
| Classification latency | 106.98 ms |
| Status | **PASS** |

**Input text tokenized:**
```
K_RAVEN (WeiyingZhao/Regularized-Recursive-Self-Improvement-of-Agent-Harnesses) — 149 files, 24642 source lines, licence Apache-2.0, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'k', '_', 'raven', '(', 'wei', '##ying', '##zh', '##ao', '/', 'regular', '##ized', '-', 'rec', '##urs', '##ive', '-', 'self', '-', 'improvement']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_