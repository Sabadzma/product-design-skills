---
name: scaffold-ux-docs
description: Set up an empty ux-docs folder for a new project or when the user wants starter files only. Use on explicit invocation or a handoff from another UX documentation skill.
---

# Scaffold UX documentation

Start on explicit invocation or when another UX documentation skill routes the user’s request here. On a handoff, follow the linked skill through completion with the same project, context, and scope. Report whether the docs already existed and what changed, including when no edits were needed.

1. Locate the target project and use `ux-docs/` at its root unless the user specifies another path. If the path points to the `ux-docs` skill package, resolve the target project before writing. If the folder already exists, use [update-ux-docs](../update-ux-docs/SKILL.md) for requested content changes. For a starter-files-only request, report the existing folder’s location and finish. If the folder is missing and the user wants populated docs, use [ux-docs](../ux-docs/SKILL.md) to create them from the supplied context. For an empty scaffold, limit inspection to locating the target and checking the output path.
2. Create exactly three files using the [shared scaffold](../ux-docs/references/folder-structure.md#empty-scaffold) when available. If the harness exposes only this skill's files, use the following layout.

   - `README.md` starts with `# UX documentation`. It links to `product-overview.md` for the product's purpose, core logic, and key capabilities and to `Glossary.md` for shared terms. It describes feature folders, where `README.md` summarizes the feature and `decisions.md` specifies detailed behavior. Mention optional `scenarios.md` for concrete situations to review when a feature has them. A shared rule lives in the `decisions.md` for the feature or product capability it governs. Dependent flows link to that rule.
   - `product-overview.md` contains only `# Product overview`.
   - `Glossary.md` contains only `# Glossary`.

3. Check that the links resolve and report the three files. Leave them ready for future content.
