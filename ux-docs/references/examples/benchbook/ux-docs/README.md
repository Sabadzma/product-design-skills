# UX documentation

The [product overview](product-overview.md) explains what Benchbook is, why workshops use it, and how it works at its core. The [glossary](Glossary.md) defines terms used across the product.

## Features

- [Equipment booking](equipment-booking/README.md)
- [Maintenance](maintenance/README.md)

Each feature's `README.md` summarizes what it does and how it works. Its `decisions.md` describes the rules, states, and exceptions that govern behavior. A feature can also include a `scenarios.md` listing situations to review.

## Shared rules

Keep each rule in the `decisions.md` of the feature that owns it. Link to that rule from dependent flows and describe their local outcomes. Update the rule at its source and check those flows when it changes.
