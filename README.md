# neokapi agent skills

Portable [Agent Skills](https://github.com/agentskills/agentskills) for
[neokapi](https://github.com/neokapi/neokapi) — install into GitHub Copilot,
Claude Code, Cursor, Windsurf, VS Code, Codex, and the rest of the SKILL.md
ecosystem with the [`skills`](https://github.com/vercel-labs/skills) CLI.

This is a **collection**, so name the skill with `--skill`:

```bash
npx skills add neokapi/agent-skills --skill kapi                    # pick your tools
npx skills add neokapi/agent-skills --skill kapi -a github-copilot  # a specific tool (repeat -a)
npx skills add neokapi/agent-skills --list                         # preview the collection
npx skills update kapi                                             # refresh later
```

Add `-g` to install user-wide instead of in the current project. You can also drop
a skill in by hand — copy its directory into your tool's skill folder
(`.github/skills/`, `.claude/skills/`, `~/.copilot/skills/`, …).

## Skills

### `kapi`

Read, edit, check, and localize the content inside any file format by driving the
local `kapi` CLI — on-brand, terminologically consistent, multilingual. The skill
drives the CLI, so install it too (`brew install neokapi/tap/kapi-cli`) and keep
it updated so the skill matches your command surface.

**Using Claude Code?** The
[Claude Code plugin](https://github.com/neokapi/claude-plugins) bundles this same
skill **plus** two hooks (a Stop hook running `kapi verify`, a PreToolUse hook
blocking hand-edits of generated targets):
`/plugin marketplace add neokapi/claude-plugins` → `/plugin install kapi@neokapi-plugins`.
For structured tool calls, run the kapi MCP server: `kapi mcp`.

## Generated, not hand-edited

Each skill is generated from the
[neokapi monorepo](https://github.com/neokapi/neokapi) (the `kapi` skill from
`cli/skills/data/kapi`) and published here on release. Edit the skill in the
monorepo, not here.
