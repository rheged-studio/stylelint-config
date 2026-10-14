---
title: Sweep Linear issue references to R and C keys
release_note: ""
version:
created_at: "2026-10-13T20:38:24Z"
merged_at: "2026-10-14T08:07:12Z"
branch: r-2743-stylelint-config-sweep-issue-references
pr: 53
commit: a7acfc4
author: rob@rheged.studio
co_authors: []
category: chore
breaking: false
issues:
  - R-2743
stats:
  files_changed: 45
  loc_added: 226
  loc_removed: 200
---

## Changed

- Rewrite legacy Linear issue references (`A-`, `SK-`, `ASW-`, `AKW-`, `WTF-`) to the new `R` and `C` keys through the committed Linear-migrate mapping ([R-2743](https://linear.app/rheged-studio/issue/R-2743))
- 44 files changed and 267 references rewritten, with no flags and nothing unmapped
- Vendored skills, changelog file names and `branch:` lines are kept verbatim by design
