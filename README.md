# PromptDriftCheck

Changed your system prompt? Paste the outputs you collected **before** and **after**, get an honest 0–100 drift score across matched sample IDs. Deterministic char-bigram Jaccard — same engine as the CLI tool [promptwake](https://github.com/qianbrady/promptwake).

**Live tool:** https://qianbrady.github.io/promptdriftcheck/ · 纯离线单文件，内容不出浏览器。

## How it works

1. Collect real outputs under your OLD prompt as JSONL: `{"id": "...", "output": "..."}` per line
2. Replay the same sample IDs against your NEW prompt
3. Paste both sides → every matched ID is scored by character-bigram Jaccard similarity; unmatched IDs are flagged, not silently dropped

Drift score `= (1 − mean_similarity) × 100`. Verdict bands: ≤15 stable · ≤40 minor · >40 major.

## Fidelity

Ported verbatim from `promptwake/core.py` and verified side-by-side in CI-style runs:
mean score matches the Python original to all decimal places on synthetic suites (e.g. 0.4624468731026108), including empty-set edge rules.

## Run locally

Open `index.html` in any browser. No build step, no network.

## License

MIT © 2025
