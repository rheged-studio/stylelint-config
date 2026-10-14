---
title: Drop the legacy A key from the skill configs
release_note: ""
created_at: "2026-10-14T13:00:35Z"
merged_at: "2026-10-14T13:05:54Z"
branch: r-2744-stylelint-config-drop-the-legacy-a-key
pr: 54
commit: d92bfd3
author: rob@rheged.studio
co_authors: []
category: chore
breaking: false
issues:
  - R-2744
stats:
  files_changed: 10
  loc_added: 37
  loc_removed: 9
  commits: 0
version: ""
---

## Changed

**Remove the legacy A issue key ([R-2744](https://linear.app/rheged-studio/issue/R-2744))**

- Set `issueKeys` to ["R"] in every skill `config.json` copy, so the legacy `A` key is no
  longer accepted now that no `a-` branches or PRs remain open.
