# Radon_Complexity_Lab_Results
**Project:** `K_RAVEN` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `10`
- **average_complexity:** `{'grade': 'B', 'score': 5.6415094339622645}`
- **complexity_grade:** `B`
- **complexity_score:** `5.6415094339622645`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_RAVEN\UPSTREAM\rrsi.py - A (59.02)
E:\fenta\Downloads\The Ant`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_RAVEN\UPSTREAM\rrsi.py
    F 158:0 dispatch - D (25)
    F 105:0 main - B (10)
    F 82:0 cmd_doctor - B (7)
    F 96:0 cmd_plan - A (2)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_RAVEN\UPSTREAM\domains\_anticloud_egress.py
    F 38:0 _is_frontier - A (4)
    F 43:0 guarded_connect - A (4)
    F 61:0 install - A (3)
    F 33:0 is_offline - A (1)
    C 29:0 EgressDenied - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_RAVEN\UPSTREAM\rrsi\analyst.py
    F 121:0 analyze - D (26)
    F 113:0 task_table - A (4)
    F 105:0 prepare_rendered - A (3)
    F 200:0 load_digests - A (3)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_RAVEN\UPSTREAM\rrsi\calibrate.py
    F 85:0 calibrate - B (9)
    F 54:0 bootstrap_se - B (8)
    F 71:0 pooled - A (4)
    F 115:0 read_delta - A (2)
    F 111:0 write - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_RAVEN\UPSTREAM\rrsi\components.py
    F 61:0 text_only - B (10)
    F 72:0 classify_diff - B (6)
    F 82:0 has_evidence - B (6)
    F 95:0 normalize - A (4)
    F 103:0 novelty - A (4)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_RAVEN\UPSTREAM\rrsi\config.py
    M 134:4 RRSIConfig.validate - C (17)
    C 88:0 RRSIConfig - B (10)
    M 121:4 RRSIConfig.load - B (9)
    F 73:0 misspelled_keys - B (7)
    F 69:0 _is_num - A (3)
    F 65:0 _is_int - A (2)
    C 61:0 ConfigError - A (1)
    M 187:4 RRSIConfig.dump
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_