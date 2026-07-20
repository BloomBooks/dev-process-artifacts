# dev-process-artifacts

Public host for **ephemeral** development-process artifacts produced by the Bloom team's
agent skills — decider forms, [preflight](https://github.com/BloomBooks/bloom-team-skills)
report pages, and screenshots destined for a PR. GitHub Pages serves the root of `main`, so
every file has a predictable URL:

```
https://bloombooks.github.io/dev-process-artifacts/<path>
```

## Why this repo exists

The Anthropic Artifact tool hosts these pages privately — readable only by the developer who
created them. When a link must be readable by anyone (a YouTrack card, a PR, a teammate, or a
zero-context agent resuming work later), the artifact is published here instead. There is
nothing special about the files: a decider is just self-contained HTML plus a little clipboard
JavaScript.

The full convention (layout, naming, publish steps, the public-vs-private tradeoff) lives in
[`dev-process-artifacts.md`](https://github.com/BloomBooks/bloom-team-skills/blob/main/dev-process-artifacts.md)
in the bloom-team-skills repo.

## Layout

```
deciders/         # decider / preflight report pages, e.g. BL-1234.html
pr-screenshots/   # images to embed in a PR
reports/          # any other one-off report pages
```

`.nojekyll` at the root tells Pages to serve files as-is — we do **not** use Jekyll.

## These links are ephemeral

Everything here is throwaway-but-linkable. The repo's history is **squashed periodically**
(e.g. yearly, or when it gets heavy with committed images), which **breaks old links**. Do not
treat a URL here as permanent — it's meant to carry a decision or a screenshot for the days or
weeks a piece of work is in flight, not to archive anything.

## Privacy

This repo is **public** — everything is world-readable and search-indexable. That's fine for
BloomDesktop/BloomPlayer content, which is already public. **Never** commit genuine secrets
(tokens, keys, customer data). Anything that must stay private belongs on the access-controlled
YouTrack card instead.
