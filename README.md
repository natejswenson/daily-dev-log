# Daily Dev Log

Daily development log entries for my personal projects. Each entry is a Markdown file
generated from that day's git commits by the [`@natjswenson/devlog`](https://github.com/natejswenson/devlog)
Claude Code skill, and rendered at [natejswenson.com/devlog](https://natejswenson.com/devlog).

This repo is the data layer: static Markdown + JSON served straight from
`raw.githubusercontent.com`, with no backend.

## Structure

```
<project>/
  manifest.json    # Index of the project's entries (newest first)
  YYYY-MM-DD.md    # One entry per day
```

**`manifest.json`**

```json
{
  "entries": [
    { "date": "2026-06-05", "file": "2026-06-05.md", "title": "…", "summary": "…" }
  ]
}
```

**Entry front matter**

```markdown
---
title: "Concise day summary"
date: 2026-06-05
project: <project>
summary: "1-2 sentence summary"
---

## What I Built
## What's Next
## Public Commits
```

## Projects

- **[1.00s](https://github.com/natejswenson/1.00s)** — dev log for the 1.00S project
- **[devlog](https://github.com/natejswenson/devlog)** — dev log for `@natjswenson/devlog`, the build-in-public skill that generates these entries
- **[linkedin-ghostwriter](https://github.com/natejswenson/linkedin-ghostwriter)** — dev log for the LinkedIn ghostwriter, a Claude skill that drafts posts in your own voice
- **[mom-im-bored](https://github.com/natejswenson/imboerd)** — dev log for the Mom I'm Bored project
- **[onetapskill](https://github.com/natejswenson/onetapskill)** — dev log for OneTap Resume, a Claude Code skill that tailors a résumé to a job and renders a PDF, free on your subscription

## How entries get here

Entries are published by running [`/devlog`](https://github.com/natejswenson/devlog) in Claude
Code (or `npx @natjswenson/devlog`). The skill reads the day's commits, writes a narrative entry,
updates the project's `manifest.json`, and pushes here. The site reads those files directly, so a
new entry is live as soon as the push lands.
