---
name: hook-variants
description: Use Soclo when the user wants distinct opening hooks as separately quoted full video adverts from a reviewed plan.
---

# Soclo hook-variants

Read the current /hook-variants playbook and references/soclo-workflow.md first. Establish the owner-approved message and the number of genuinely different hooks. Each variant is a separate complete film, not a cheap opening-only edit.

Use soclo_host_plan_prepare, read its chosen guides, and author/import a distinct saved storyboard for each hook. Give every item a distinct projectId and stable clientRequestId; preserve its actual revision and selected source versions. Use soclo_video_variants_quote to quote those saved projects in pages allowed by the current schema.

Show each full-film quote and the total, with wallet observations clearly labelled as estimates rather than reservations. Wait for the owner's approval of each exact item. soclo_video_variants_approve purchases one approved item per call; never blanket-approve unselected items. Use soclo_video_variants_status and soclo_video_recover for original items until actual delivery, especially after unknown outcomes. Compare only returned results and never invent a winning hook.
