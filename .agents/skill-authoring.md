# Authoring product design skills

Author project skills using the [Agent Skills specification](https://agentskills.io/specification). Keep `SKILL.md` frontmatter within the spec, use skill-relative links, and include all shared resources in the skill folder. Describe the capabilities the workflow needs and treat named tools or design apps as examples when the workflow can use equivalent sources.

Keep installation paths, command syntax, and harness-specific settings out of the shared instructions. Optional harness configuration may accompany the skill when the workflow works without it. Validate the shared package against the spec and check its resource links before release.

## UX documentation skills

Keep these four skill folders together when installing the set. The `ux-docs` skill folder holds the templates and reference, and each skill operates on the target project's separate `ux-docs/` folder.

| Skill | When to use it |
|---|---|
| `scaffold-ux-docs` | Set up starter files for later. |
| `ux-docs` | Create the project's first UX docs from existing materials. |
| `update-ux-docs` | Record decisions and discussed scenarios or maintain existing UX docs. |
| `explore-ux-scenarios` | Explore situations for design review and save them when requested. |

Maintain the four skills as a set. When changing one, check which other workflows can encounter the same situation or rely on the same logic. Apply and verify the change in every affected skill in the same pass. Put shared behavior in a common reference or template where practical.

## Explicit invocation

For a skill the user wants to invoke manually, state that requirement in both its description and instructions. The Agent Skills specification has no shared setting that enforces it. Use the target harness's invocation policy when it provides one.

To keep unused skills out of the session context across harnesses, store the skill folders outside automatic discovery paths. When you want to use a skill, ask the agent to read and use its `SKILL.md` and give it access to the whole folder. For example, ask it to use `skills/scaffold-ux-docs/SKILL.md`.

If you prefer native invocation in a particular harness, use its manual-only configuration.

| Harness | Manual-only setup |
|---|---|
| Codex | Keep each skill's `agents/openai.yaml` with `policy.allow_implicit_invocation: false`. Invoke with `$skill-name`. [Codex skills](https://developers.openai.com/codex/skills) |
| Claude Code | Where supported, set each skill's entry in `skillOverrides` to `user-invocable-only` in Claude Code settings. Alternatively, add `disable-model-invocation: true` to the installed copy's `SKILL.md` frontmatter. Invoke with `/skill-name`. [Claude Code skills](https://code.claude.com/docs/en/skills#control-who-invokes-a-skill) |
| Cursor and Copilot in VS Code | Add `disable-model-invocation: true` to each installed copy's `SKILL.md` frontmatter. Invoke with `/skill-name`. [Cursor skills](https://cursor.com/docs/skills) and [VS Code skills](https://code.visualstudio.com/docs/agent-customization/agent-skills#_use-skills-as-slash-commands) |

## Updating a skill and preparing its release

1. Start from current `main`. In a clean checkout on `main`, run `git pull --ff-only` to pick up earlier releases. Preserve any work already in progress.
2. Edit the package under `skills/<skill-name>/`. Check affected templates, examples, and handoffs. Run `npx skills add . --list` from the repository root to verify discovery, then exercise the changed workflow on a sample project.
3. For a user-facing change, run `npm ci` if dependencies need installing, then `npm run changeset`. Choose a patch for a compatible fix, a minor bump for a compatible addition, or a major bump for a breaking change. Describe the effect on the designer using the skill. All four skills share the package version.
4. Include the generated `.changeset/*.md` file in the same commit or pull request as the skill edits. When the change reaches `main`, the [release workflow](../.github/workflows/release.yml) prepares or updates the **chore: version skills** pull request. It combines pending changesets, updates the version, and writes the changelog.
5. When the maintainer is ready to publish, merge the version pull request. Verify the release workflow succeeds and the tag appears on GitHub. Sync local `main` before starting the next update.
