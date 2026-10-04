# Deploy Guide — K_RAVEN
**Tier:** TIER_4_INFERENCE_AGENTS | **Stack:** Python 3.11, PyTorch 2.10+, small draft model (1.5B), PAX 27B (verifier), AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, PyTorch 2.10+, T4 GPU (fits draft + PAX Q4 together in 15.6GB VRAM), CUDA 12.x.

## Environment
T4 GPU: draft model (1.5B, ~3GB VRAM) + PAX 27B Q4 (~8GB VRAM) = ~11GB total. CUDA 12.x.

## AIOSS Integration
```bash
aioss init --module K_RAVEN --output ./k_raven.aioss
aioss append --chain ./k_raven.aioss --payload ./output.bin --module K_RAVEN
aioss verify --chain ./k_raven.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="K_RAVEN",
    aioss_chain="./K_RAVEN.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_RAVEN.aioss --verbose
python -m K_RAVEN.tests.smoke
```
