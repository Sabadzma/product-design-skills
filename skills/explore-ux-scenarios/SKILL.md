---
name: explore-ux-scenarios
description: Explore real situations a feature, flow, or screen may encounter during use. Use only when the user explicitly requests the explore-ux-scenarios skill.
---

# Explore UX scenarios

Run this skill only when the user explicitly asks to use it. A documentation handoff or a mention of scenarios alone does not invoke it. Start with the feature, flow, or screen the user named. Read its relevant UX docs and existing scenarios, using the design or discussion for context when available.

Walk through the ordinary flow, then vary a condition the design relies on. Consider what may be absent, delayed, interrupted, or changed by another person. Keep a situation when a designer could cover the ordinary flow and still miss it. “A user reassigns a promise” repeats a capability. “The user reassigns a promise while the previous delegate submits a completion update” exposes a timing and ownership question. Ground candidates in the feature’s actual actors and actions.

Return one bullet per distinct situation in chat. Use only headings with credible examples. Place each situation under its most useful heading once.

- **Empty states** — Name what is absent in one short sentence. Add the cause only when it distinguishes a different experience. “There are no active projects in the workspace.”
- **Loading and pending states** — Describe the action underway and what the person sees, does, or is waiting for before the result arrives.
- **Error and recovery states** — State the failure and its immediate consequence in a short sentence. “The connection drops while the editor is saving, and the changes fail to save.” If the outcome is unknown, say so.
- **Edge cases** — Describe the specific combination or sequence that could break an assumption, such as competing edits, changing access, or an action crossing a time boundary.

A scenario can stand alone. Add solutions, UI copy, or expected behavior only on request. Use the [Pages example](references/examples/pages/scenarios.md) as a guide to the differences in length and detail.

When asked to save, merge the selected situations into the owning feature’s `scenarios.md` in the target project's UX docs. Use a feature title and bullets, reuse matching entries, preserve unrelated content, and link the list from the feature README. Link to a relevant confirmed rule when useful. If the user agrees on a behavior and wants to record it as a decision in the UX docs, follow [update-ux-docs](../update-ux-docs/SKILL.md) for that decision and report the result.
