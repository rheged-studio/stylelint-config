---
title: Re-vendor agent-skills v1.13.0 with R and A issue keys
release_note: ""
version:
created_at: "2026-10-13T13:39:00Z"
merged_at: "2026-10-13T13:32:12Z"
branch: a-2768-stylelint-config-re-vendor-the-multi-team-skills-and
pr: 51
commit: 522ec61
author: rob@rheged.studio
co_authors: []
category: chore
breaking: false
issues:
  - R-2768
  - R-2742
affected_packages:
  - infrastructure
stats:
  files_changed: 82
  loc_added: 2559
  loc_removed: 971
---

## Changed

**Re-vendor the multi-team skills ([R-2768](https://linear.app/rheged-studio/issue/R-2768))**

- Re-vendor the Rheged and Matt Pocock bundles into `.claude` and `.agents` from agent-skills v1.13.0, restoring each `config.json` after `--copy` ([R-706](https://linear.app/rheged-studio/issue/R-706))
- Bump the `@rheged-studio/changelog-core` devDependency to `^1.2.0`

**Set R and A issue keys ([R-2742](https://linear.app/rheged-studio/issue/R-2742))**

- Set `issueKeys` to `["R", "A"]` in the root `config.json` and the changelog, cleanup-repo, Linear-sync and triage-pr skill configs
