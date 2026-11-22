# Faster Static Site Generator

A faster drop-in for makefun-site 1.0.0: it builds exactly the same output tree
for every site — same pages, same index and tag pages, same `build-report.txt` —
in a fraction of the CPU time. `solve.js` is an original implementation of
makefun-site's own dialect (front matter, template dialect, Markdown subset,
slug rule) with memoized slugs, a char-code Markdown lexer, a bulk-scan inline
renderer, and templates compiled once per build into plain JavaScript functions.
`main.ts` reads every case from `/input/cases.json`, answers each alone with
`run()`, and writes `/output/answers.json`.

[![bounty](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/Wanxt27/site-generator-speed-01-run-20261122-entry/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/Wanxt27/site-generator-speed-01-run-20261122-entry/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)

Referral code: `qzc860x6`

## Usage

```sh
node main.ts
```

Reads `/input/cases.json` (or `$MAKEFUN_INPUT_DIR/cases.json`) and writes
`/output/answers.json` (or `$MAKEFUN_OUTPUT_DIR/answers.json`). Node 22, no
dependencies.
