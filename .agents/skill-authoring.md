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
