# Product Design Skills

Four agent skills for designers who want to carry UX decisions from a design conversation into their project. They create and maintain Markdown documentation and help you explore situations a feature may encounter in use.

## Install

From the project where you want to use the skills, run the following command. Install all four together so the agent can follow handoffs and find the shared templates.

```sh
npx skills add Sabadzma/product-design-skills --skill '*'
```

## Choose a skill

| Skill | When to use it |
| --- | --- |
| [scaffold-ux-docs](scaffold-ux-docs/SKILL.md) | Start a new project with a documentation guide, an empty product overview, and a glossary to fill in later. |
| [ux-docs](ux-docs/SKILL.md) | Turn existing designs, project materials, and agreed decisions into a first set of UX docs. If docs already exist, the agent follows the update workflow. |
| [update-ux-docs](update-ux-docs/SKILL.md) | Capture decisions and scenarios from a conversation, then update the affected features and references. |
| [explore-ux-scenarios](explore-ux-scenarios/SKILL.md) | Ask explicitly for situations to consider when reviewing a feature, flow, or screen. The skill returns a list in chat and saves scenarios when asked. |

## Example workflow

After designing a page list with your agent, you could ask:

1. “Use `ux-docs` to document the Pages flow we just designed.”
2. “Use `explore-ux-scenarios` to list situations we should consider when someone filters the page list.”
3. “Use `update-ux-docs` to record our decision: when filters hide every page, keep the active filters visible and offer Clear filters.”

The resulting `ux-docs/` folder has a product overview and glossary. Each documented feature has a README and can include a `decisions.md` for agreed behavior and a `scenarios.md` for situations worth reviewing. A scenario can be recorded before the team chooses a response.

See the [Benchbook example](ux-docs/references/examples/benchbook/ux-docs/README.md) for a complete set of sample docs.

## Releasing changes

All four skills share a version. After changing a skill, run `npm ci` and then `npm run changeset` to describe the change and choose a version bump. Commit the generated changeset with your edits. On GitHub, merge the version pull request when the collection is ready to release.
