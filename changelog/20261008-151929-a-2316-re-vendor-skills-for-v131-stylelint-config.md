---
title: Re-vendor agent skills for mattpocock/skills v1.3.1
release_note: ""
version:
created_at: "2026-10-08T15:19:29Z"
merged_at:
branch: a-2316-re-vendor-skills-for-v131-stylelint-config
pr:
commit:
author: rob@rheged.studio
co_authors: []
category: chore
breaking: false
issues:
  - A-2316
affected_packages:
  - infrastructure
stats:
  files_changed:
  loc_added:
  loc_removed:
---

## Changed

**Re-vendor shared skills for v1.3.1 ([A-2316](https://linear.app/rheged-studio/issue/A-2316))**

- Roll Rheged and Matt Pocock bundles on `.claude` and `.agents` mirrors via `fleet-update.mjs`
- Add `implement-spec`, `retro`, and Rheged `pr`; remove upstream-dropped `resolving-merge-conflicts`
- Restore per-skill `config.json` after `--copy` ([A-706](https://linear.app/rheged-studio/issue/A-706)); keep `triage-pr` on unattended Phase B (`humanEnvelope: false`) and `follow-up` follow-up label
- Refresh `skills-lock.json` / `.claude/skills.lock` to current GitHub provenance ([A-718](https://linear.app/rheged-studio/issue/A-718))
