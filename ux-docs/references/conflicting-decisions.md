# Handle conflicting UX decisions

Use this workflow when in-scope sources give incompatible answers about the same behavior under the same conditions and a confirmed decision has yet to settle the difference. Treat observed current behavior and an agreed redesign target as separate contexts.

Ask before writing and wait for the user's choice.

> Some sources describe different behavior for the same UX decisions. Would you like to resolve those differences one at a time, or list them under Open questions for later?

- **Resolve them one at a time.** Present the options and their sources for one decision. Wait for the user's answer before asking about the next conflict. Use each confirmed answer as the decision to document. Save anything the user defers as an open question.
- **List them as open questions.** In the owning feature's `decisions.md`, add one item per conflict under `## Open questions`. State the question and the competing options briefly, and cite or link each source. Update a matching open question in place.

For existing docs, keep the current rule in effect until the user confirms a replacement. When a question is resolved, record the confirmed behavior, update its dependent flows, and remove the corresponding open question. Continue documenting other in-scope decisions once the user has chosen how to handle conflicts.
