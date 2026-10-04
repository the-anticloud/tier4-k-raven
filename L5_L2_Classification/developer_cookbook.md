# Developer Cookbook — K_RAVEN
**Stack:** Python 3.11, PyTorch 2.10+, small draft model (1.5B), PAX 27B (verifier), AIOSS_FORMAT
**Domain:** Speculative decoding accelerator: draft-verify inference speedup for PAX 27B

## Speculative decoding inference
```python
from k_raven import RavenSpecDecoder

decoder = RavenSpecDecoder(
    draft_model="./raven-draft-1.5b.gguf",
    verifier_model="./pax-27b-q4.gguf",
    gamma=5,  # draft tokens per step
    aioss_chain="./raven.aioss"
)

result = decoder.generate(
    prompt="Analyze this EEG signal for seizure patterns:",
    max_tokens=256
)
print(result.text)
print(f"Speedup: {result.speedup:.1f}x, Acceptance rate: {result.acceptance_rate:.2%}")
print(f"Chain: {result.chain_hash}")
```

## Benchmark speedup
```python
bench = decoder.benchmark(n_tokens=1000, n_trials=5)
print(f"Speculative: {bench.spec_tokens_per_sec:.1f} tok/s")
print(f"Baseline: {bench.base_tokens_per_sec:.1f} tok/s")
print(f"Speedup: {bench.speedup:.1f}x")
```

## Tune draft length (gamma)
```python
for gamma in [3, 5, 7, 9]:
    bench = decoder.benchmark(gamma=gamma)
    print(f"gamma={gamma}: {bench.speedup:.1f}x speedup, {bench.acceptance_rate:.2%} acceptance")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
