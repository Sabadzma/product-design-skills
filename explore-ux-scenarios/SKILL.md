---
name: explore-ux-scenarios
description: Explore real situations a feature, flow, or screen may encounter during use. Use only when the user explicitly requests the explore-ux-scenarios skill.
---

# Explore UX scenarios

Run this skill only when the user explicitly asks to use it. A documentation handoff or a mention of scenarios alone does not invoke it. Start with the feature, flow, or screen the user named. Read its relevant UX docs and existing scenarios, using the design or discussion for context when available.

Trace what a person is trying to do and what they depend on at each step. Look for realistic changes in timing, data, access, or context that would affect their experience. For example, a list can appear empty because a branch has no pages, because filters hide every page, or because the total is still loading. Follow distinctions that matter to this design.

Return a concise list in chat. Describe each distinct situation in one concrete bullet. Group by activity if it makes a longer list easier to use. The [Pages example](references/examples/pages/scenarios.md) illustrates activity groups and standalone situations. Supply possible responses or assess coverage when requested, and distinguish suggestions from documented behavior.

When asked to save, merge the selected situations into the owning feature’s `scenarios.md` in the target project's UX docs. Use a feature title and bullets, reuse matching entries, preserve unrelated content, and link the list from the feature README. Link to a relevant confirmed rule when useful. If the user agrees on a behavior and wants to record it as a decision in the UX docs, follow [update-ux-docs](../update-ux-docs/SKILL.md) for that decision and report the result.
