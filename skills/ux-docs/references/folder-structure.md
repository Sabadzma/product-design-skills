# UX documentation structure

Use this layout for new project documentation.

- `ux-docs/`
  - `README.md`
  - `product-overview.md`
  - `Glossary.md`
  - `<feature>/`
    - `README.md`
    - `decisions.md`
    - `scenarios.md` (optional)

## File roles and templates

| Project file | Purpose | Template |
|---|---|---|
| `ux-docs/README.md` | Explain the folder layout, the role of each file, and how to maintain shared rules. | Root variant of [readme.md](../assets/templates/readme.md) |
| `ux-docs/product-overview.md` | Describe the product, its purpose, its core logic, and its key capabilities. | [product-overview.md](../assets/templates/product-overview.md) |
| `ux-docs/Glossary.md` | Define product terms that readers need to recognize across features. Link to the relevant behavior where a term has operational consequences. | [glossary.md](../assets/templates/glossary.md) |
| `ux-docs/<feature>/README.md` | Explain what the feature does, summarize its core logic, and link to relevant sections in its decisions. | Feature variant of [readme.md](../assets/templates/readme.md) |
| `ux-docs/<feature>/decisions.md` | Describe the agreed behavior, relevant states and exceptions, and the reasoning behind consequential choices. | [decisions.md](../assets/templates/decisions.md) |
| `ux-docs/<feature>/scenarios.md` | Collect concrete situations to consider while designing or reviewing a feature. | [scenarios.md](../assets/templates/scenarios.md) |

Copy the relevant variant of `readme.md` into `README.md` and omit the variant markers. Keep the output filenames and capitalization shown above. Fill the `{{...}}` placeholders using available information and remove unused example sections and links. Adapt existing documents in place and use the decision format for entries you create or revise.

Name new feature folders after the domain or capability, using lowercase hyphenated names. Keep closely related flows together when they share core logic. For example, ownership transfer, role changes, and leaving a project can live in `project-membership/`. Create a feature's `decisions.md` when there is detailed behavior or an open decision in scope, or when the user asks to scaffold that feature. Add links when their targets exist.

## Empty scaffold

Create these three files in `ux-docs/`.

- `README.md` uses the root variant of [readme.md](../assets/templates/readme.md), with the guide and its links intact.
- `product-overview.md` starts with `# Product overview`.
- `Glossary.md` starts with `# Glossary`.

Leave the overview and glossary empty beneath their titles. Feature folders and decision files are added when there is content to document or the user asks to scaffold a named feature.

## Product overview

Start with a short description of what the product is and why people use it. Explain its shared logic in a short paragraph and list the key features in one sentence each. Include the capabilities a reader needs to understand the product's purpose. Keep screens, individual flows, and detailed rules in the feature docs.

When project context becomes available, fill a missing, empty, or placeholder-only overview using what the sources or existing UX docs support. Write a useful partial overview when only some product-level facts are known. Omit empty sections and tell the user what information is missing.

During maintenance, add or revise the relevant part when a source establishes a meaningful detail about the product's purpose, core logic, or key features. Follow the user's scope for any requested overview edits. In Benchbook, learning that reservations and maintenance share one schedule adds a sentence to Core logic. The appearance of an overlap warning belongs in the maintenance feature docs.

## Feature scenarios

Initial UX documentation covers known behavior in the feature docs. Scenario discovery belongs to an explicitly requested `explore-ux-scenarios` pass. Save explored scenarios when requested. During a direct update, `update-ux-docs` may also record concrete situations the user raised or selected for design review.

Link a saved list from the feature README. Use only categories with entries. Empty states briefly name what is absent. Error and recovery states briefly name what failed and its consequence. Loading and pending states describe what happens while an outcome is pending. Edge cases describe interacting conditions or events. Use one bullet per situation. A relevant confirmed decision can be linked using a relative path.

## Decision format

Use the [decisions template](../assets/templates/decisions.md) for entries. Give each rule or flow one descriptive `##` heading. Write a behavior paragraph of one to three sentences and up to 60 words. Add one separate rationale sentence of up to 25 words when the source explains a consequential choice. Count visible prose, excluding headings and link destinations. Keep open questions in their own section when tracking them is in scope.

- Extract the behavior from source material and group it by the rules and flows it affects. Use the existing decision headings where they still fit. Ignore the source's outline and formatting, including screen-by-screen sections, tables, and acceptance criteria lists.
- Write in plain, active, present-tense language, using terms from the project's docs. State what triggers the rule, which conditions apply, and what happens. Include a state, exception, or UI detail only when it changes available actions, the outcome, or what the user needs to know to proceed. Keep examples and implementation details in the source. Link to the source if those details are needed.
- Put a shared rule in its owning feature's `decisions.md`. In dependent flows, link to it and document the local outcome. If two behaviors need separate conditions or outcomes, give them their own headings. Keep the sections you touch within the format and word limits.

## Decide where a rule belongs

Look for an existing rule first. Give each detailed rule a home in the `decisions.md` for the feature or product capability it governs. In Benchbook, Maintenance owns when a block takes effect. Equipment booking links to that rule and describes what members can book or reschedule.

## Worked example

Benchbook is a fictional equipment booking product for community workshops. Read the files that match the documents you are writing. Use their structure and level of detail as a guide. Use the target project's own terms and evidence for its content.

| Document type | Example |
|---|---|
| Root guide | [UX documentation](examples/benchbook/ux-docs/README.md) |
| Product overview | [Product overview](examples/benchbook/ux-docs/product-overview.md) |
| Glossary | [Glossary](examples/benchbook/ux-docs/Glossary.md) |
| Feature overview | [Equipment booking](examples/benchbook/ux-docs/equipment-booking/README.md) and [Maintenance](examples/benchbook/ux-docs/maintenance/README.md) |
| Decisions | [Equipment booking decisions](examples/benchbook/ux-docs/equipment-booking/decisions.md) and [Maintenance decisions](examples/benchbook/ux-docs/maintenance/decisions.md) |
| Scenarios | [Equipment booking scenarios](examples/benchbook/ux-docs/equipment-booking/scenarios.md) |
