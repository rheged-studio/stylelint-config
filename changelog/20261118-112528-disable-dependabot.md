---
title: Remove the Dependabot configuration
release_note: ""
created_at: "2026-11-18T11:25:28Z"
merged_at: "2026-11-18T11:53:02Z"
branch: disable-dependabot
pr: 57
commit: c6e20f2
author: rob@rheged.studio
co_authors: []
category: chore
breaking: false
issues: []
stats:
  files_changed: 2
  loc_added: 25
  loc_removed: 36
  commits:
version: ""
---

## Changed

- Removed `.github/dependabot.yml`: Dependabot is switched off across the estate, so this repo
  no longer receives automated dependency or GitHub Actions bump PRs.
