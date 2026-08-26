# PromptDriftCheck

![License](https://img.shields.io/badge/license-MIT-green) ![Offline](https://img.shields.io/badge/network-none-blue) ![Live](https://img.shields.io/badge/try%20it-online-8A2BE2)

Score how much your LLM outputs moved after a system prompt change (0-100 drift).

**Try it now:** <https://qianbrady.github.io/promptdriftcheck/> - single-file web tool, nothing leaves your browser.

## Install

No dependencies. Grab the file:

```bash
git clone https://github.com/qianbrady/promptdriftcheck.git
```

Then open `index.html` in any browser.

## Quickstart

1. Open the live page (or local `index.html`)
2. Paste your content into the input box
3. Press the primary button
4. Read the score / result panel

## Usage

```
Input : your pasted text (see placeholder for exact format)
Output: score panel + per-item breakdown + copyable Markdown where applicable
```

Deterministic char-bigram Jaccard, matched by sample ID; unmatched IDs flagged, never dropped.

## Contributing

Issues and PRs welcome - this is a zero-dependency static page, so any text editor is a complete dev environment.

## License

[MIT](LICENSE) (c) 2025