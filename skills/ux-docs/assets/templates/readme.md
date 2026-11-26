<!-- root -->
# UX documentation

This guide explains how the UX documentation is organized and where to document changes.

## Product-wide files

- [Product overview](product-overview.md) briefly explains what the product is, what it is for, how it works at its core, and its key capabilities.
- [Glossary](Glossary.md) defines terms used across the product and links to relevant rules where those terms affect behavior.

## Feature folders

Each feature folder covers a feature or a group of flows that share core logic.

- `README.md` explains what the feature does, summarizes its core logic, and links to the relevant decisions.
- `decisions.md` defines how the feature behaves in specific situations, including flows, states, and edge cases. It includes rationale when it helps explain a choice.
- An optional `scenarios.md` lists situations to consider during design review.

## Rules shared across features

Give each detailed rule one authoritative home in the `decisions.md` for the feature or product capability it governs. Where another feature depends on a rule, link to the specific section and explain what happens in that feature's flow.

When a rule changes, update it at its source and review the flows that reference it.
<!-- /root -->

<!-- feature -->
# {{Feature name}}

{{Explain what the feature does and what users can accomplish with it.}}

{{Summarize the feature's core logic and group related flows in this overview.}}

See [{{Decision title}}](decisions.md#{{decision-heading-slug}}) for the detailed behavior.
<!-- /feature -->
