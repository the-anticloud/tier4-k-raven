# 3-Seed Simulation — K_RAVEN

**Seeds:** `44085` · `75422` · `9621`

**Seed method:** `sha256("K_RAVEN")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `K_RAVEN`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 7.081 | 0.1737 | ±0.3405 |
| throughput_tokens_per_sec | 648.0333 | 23.7981 | ±46.6443 |
| p50_latency_ms | 45.18 | 2.6384 | ±5.1713 |
| p99_latency_ms | 110.2367 | 12.6514 | ±24.7967 |
| ttft_ms | 30.7 | 1.2385 | ±2.4275 |
| mmlu_proxy | 0.7561 | 0.0304 | ±0.0596 |
| hellaswag_proxy | 0.7692 | 0.0302 | ±0.0592 |
| truthfulqa_proxy | 0.5633 | 0.0204 | ±0.04 |
| arc_proxy | 0.708 | 0.0388 | ±0.076 |
| complexity_cyclomatic | 4.53 | 0.2922 | ±0.5727 |
| maintainability_index | 67.8933 | 4.1201 | ±8.0754 |
| security_issues_high | 0.3333 | 0.4714 | ±0.9239 |
| dependency_freshness_pct | 80.6333 | 2.2647 | ±4.4388 |
| test_coverage_pct | 66.6333 | 3.8003 | ±7.4486 |
| doc_coverage_pct | 60.7667 | 5.9779 | ±11.7167 |
| memory_mb | 50.0 | 0.0 | ±0.0 |
| gpu_util_pct | 67.6333 | 5.0658 | ±9.929 |
| openssf_score | 6.1567 | 0.4781 | ±0.9371 |
| eu_ai_act_compliance_pct | 79.5667 | 6.3908 | ±12.526 |
| slsa_level | 1.0 | 0.0 | ±0.0 |

## Per-Seed Raw Results

| Metric | Seed 44085 | Seed 75422 | Seed 9621 |
|--------|------------|------------|------------|
| trl_score | 7.188 | 7.219 | 6.836 |
| throughput_tokens_per_sec | 681.2 | 626.5 | 636.4 |
| p50_latency_ms | 41.47 | 46.69 | 47.38 |
| p99_latency_ms | 117.54 | 120.73 | 92.44 |
| ttft_ms | 29.33 | 32.33 | 30.44 |
| mmlu_proxy | 0.7776 | 0.7775 | 0.7131 |
| hellaswag_proxy | 0.8058 | 0.77 | 0.7319 |
| truthfulqa_proxy | 0.5901 | 0.5592 | 0.5406 |
| arc_proxy | 0.6533 | 0.7395 | 0.7311 |
| complexity_cyclomatic | 4.78 | 4.69 | 4.12 |
| maintainability_index | 64.95 | 73.72 | 65.01 |
| security_issues_high | 0 | 1 | 0 |
| dependency_freshness_pct | 78.3 | 83.7 | 79.9 |
| test_coverage_pct | 64.2 | 63.7 | 72.0 |
| doc_coverage_pct | 62.3 | 67.2 | 52.8 |
| memory_mb | 50 | 50 | 50 |
| gpu_util_pct | 73.7 | 67.9 | 61.3 |
| openssf_score | 6.25 | 5.53 | 6.69 |
| eu_ai_act_compliance_pct | 88.6 | 74.8 | 75.3 |
| slsa_level | 1 | 1 | 1 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._