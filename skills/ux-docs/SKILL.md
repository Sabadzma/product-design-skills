---
name: ux-docs
description: Create and populate a project's first ux-docs folder from existing designs, product materials, and agreed decisions. Use on explicit invocation or a handoff from another UX documentation skill.
---

# Create UX documentation from existing materials

Start on explicit invocation or when another UX documentation skill routes the user’s request here. On a handoff, follow the linked skill through completion with the same project, context, and scope. Report whether the docs already existed and what changed, including when no edits were needed.

1. Identify the target project and its documentation path. Default to `ux-docs/` at the project root. If the path points to this skill package, resolve the target project before writing. If the folder already exists and the request is for starter files only, report its location. For any requested documentation work in an existing folder, use [update-ux-docs](../update-ux-docs/SKILL.md) to apply the requested changes. If the folder is missing and the user wants only starter files, use [scaffold-ux-docs](../scaffold-ux-docs/SKILL.md). Otherwise continue below.
2. Review relevant available sources, such as project docs, designs, implemented flows, and decisions the user has confirmed. Treat visible or implemented behavior as observed. Clearly label an agreed redesign target where it differs from current behavior. Keep unresolved permissions, defaults, or transitions open and link to sources when they help verify the behavior.
3. If sources give conflicting answers to the same UX decision under the same conditions and no confirmed choice settles the conflict, follow the [conflict workflow](references/conflicting-decisions.md) before writing the docs.
4. Use the [folder structure and templates](references/folder-structure.md) to create the three starter files and populate them with supported details. Write a [product overview](references/folder-structure.md#product-overview) with the known purpose, core logic, and key capabilities. Add feature folders for the capabilities you can document. Use feature READMEs for summaries and core logic, and follow the [decision format](references/folder-structure.md#decision-format) for `decisions.md` entries. Give each detailed rule one home and link to it from dependent flows. Keep unresolved alternatives in `## Open questions`.
5. Capture concrete scenarios raised in the in-scope discussion or source materials using the [scenario format](references/folder-structure.md#feature-scenarios). If the user also explicitly requested [explore-ux-scenarios](../explore-ux-scenarios/SKILL.md), run it after completing the documentation.
6. Compare the generated documents with the [worked example](references/folder-structure.md#worked-example) and check their relative links. Tell the user what you documented, any overview details you could not establish, and which decisions remain open.
