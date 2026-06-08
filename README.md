# AI Agent Skills

Local snapshots of useful skills and playbooks for Codex, Claude Code, Cursor,
OpenCode, and other `SKILL.md`-compatible agents.

## Collections

- [`collections/ok-skills`](collections/ok-skills/README.md): 47 practical
  community skills. Includes
  [`caveman`](collections/ok-skills/caveman/SKILL.md),
  [`planning-with-files`](collections/ok-skills/planning-with-files/SKILL.md),
  [`systematic-debugging`](collections/ok-skills/systematic-debugging/SKILL.md),
  and [`tdd`](collections/ok-skills/tdd/SKILL.md).
- [`collections/ok-skills/CLAUDE_AGENTS.md`](collections/ok-skills/CLAUDE_AGENTS.md):
  a reusable `CLAUDE.md` / `AGENTS.md` playbook. Review and adapt it before
  making it active in a project.
- [`collections/openai-skills`](collections/openai-skills/README.md): 44
  official OpenAI skills, including curated and system skills.
- [`collections/anthropic-skills`](collections/anthropic-skills/README.md): 18
  official Anthropic skills plus the Agent Skills specification and template.
- [`collections/awesome-agent-skills`](collections/awesome-agent-skills/README.md):
  a maintained catalog for finding additional third-party skills.

## Installation & Usage

Each AI agent discovers skills from either a **Global Path** (applies across all your workspaces) or a **Project Path** (applies only to the current repository). To install any skill from this repository, copy its directory (containing the `SKILL.md` file) to the appropriate location:

### CLIs

| Tool | Project Path | Global Path |
| :--- | :--- | :--- |
| **Antigravity CLI** | `.agent/skills/` | `~/.gemini/antigravity/skills/` |
| **Codex CLI** | `.agents/skills/` | `~/.agents/skills/` |
| **Anthropic CLI (Claude Code)** | `.claude/skills/` | `~/.claude/skills/` |

#### Anthropic CLI (Claude Code) Plugin Marketplace
Alternatively, you can register and install the official Anthropic skills directly in Claude Code:
```bash
/plugin marketplace add anthropics/skills
/plugin install example-skills@anthropic-agent-skills
```

---

### IDEs & VS Code Extensions

#### Antigravity IDE
* **How it works:** Automatically discovers and loads skills from the global path (`~/.gemini/antigravity/skills/`) and project path (`.agents/skills/` or `.agent/skills/`).
* **Setup:** Place skill folders in either path. The IDE uses progressive disclosure to automatically select and apply relevant skills based on the active task and files.

#### Codex VS Code Extension
* **How it works:** Reads active skills from the project's `.agents/skills/` or `.codex/skills/` directories.
* **Setup:** Copy the desired skill folder (e.g., `tdd/`) into `.agents/skills/` in your workspace. You can also specify agent behaviors in an `AGENTS.md` file in the workspace root.

#### Anthropic VS Code Extension
* **How it works:** Reads project-specific instructions and skills from the `.claude/skills/` folder.
* **Setup:** Copy skill folders into `.claude/skills/` at the root of your workspace. Project-wide preferences can also be declared in a `CLAUDE.md` file in the workspace root.

#### Cursor
* **Project Skills:** Copy skill folders containing `SKILL.md` to `.cursor/skills/` in your workspace root.
* **Project Rules (`.cursorrules` / `.mdc` files):** Put rules in `.cursor/rules/` as `.mdc` markdown files. You can create them via the Command Palette (`Cmd/Ctrl + Shift + P` -> `New Cursor Rule`).
* **Global Rules:** Enter rules in Cursor Settings under **Rules for AI**.

---

There are 109 runnable `SKILL.md` files in this repository. Third-party skills can contain scripts or tool instructions, so review a skill before enabling or running it.

See [`SOURCES.md`](SOURCES.md) for upstream repositories and pinned revisions.
