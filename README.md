# Claude Code — Job28703's Plugin Fork

> Fork of [anthropics/claude-code](https://github.com/anthropics/claude-code) · Personal plugin collection & workflow extensions

[![Node.js 18+](https://img.shields.io/badge/Node.js-18%2B-brightgreen?style=flat-square)](https://nodejs.org) [![npm](https://img.shields.io/npm/v/@anthropic-ai/claude-code.svg?style=flat-square)](https://www.npmjs.com/package/@anthropic-ai/claude-code)

Claude Code is Anthropic's agentic coding tool that lives in your terminal. This fork extends the official release with **13 custom plugins**, specialized slash commands, and DevContainer tooling.

**Install the official CLI → [code.claude.com/docs/en/setup](https://code.claude.com/docs/en/setup)**

---

## ✨ What's added in this fork

| Asset | Count | Location |
|---|---|---|
| Custom plugins | 13 | [`plugins/`](./plugins/) |
| Custom slash commands | 3 | [`.claude/commands/`](./.claude/commands/) |
| DevContainer script | 1 | [`scripts/`](./scripts/) |
| GitHub automation scripts | 3 | [`scripts/`](./scripts/) |

---

## 🔌 Plugins

See [`plugins/README.md`](./plugins/README.md) for full documentation on each plugin.

| Plugin | Type | What it does |
|---|---|---|
| [**agent-sdk-dev**](./plugins/agent-sdk-dev/) | Command | Scaffolds new Claude Agent SDK apps (`/new-sdk-app`) |
| [**claude-opus-4-5-migration**](./plugins/claude-opus-4-5-migration/) | Skill | Migrates code from Sonnet 4.x / Opus 4.1 to Opus 4.5 |
| [**code-review**](./plugins/code-review/) | Command | Parallel PR review with 5 Sonnet sub-agents (`/code-review`) |
| [**commit-commands**](./plugins/commit-commands/) | Command | Git workflow automation (`/commit`, `/commit-push-pr`, `/clean_gone`) |
| [**explanatory-output-style**](./plugins/explanatory-output-style/) | Hook | SessionStart hook that injects educational coding context |
| [**feature-dev**](./plugins/feature-dev/) | Command | 7-phase guided feature development (`/feature-dev`) |
| [**frontend-design**](./plugins/frontend-design/) | Skill | Production-grade UI/UX design (auto-invoked) |
| [**hookify**](./plugins/hookify/) | Command | Create & manage custom hooks (`/hookify`, `/hookify:list`) |
| [**learning-output-style**](./plugins/learning-output-style/) | Hook | SessionStart hook that encourages meaningful contributions |
| [**plugin-dev**](./plugins/plugin-dev/) | Command | Full plugin creation toolkit (`/plugin-dev:create-plugin`) |
| [**pr-review-toolkit**](./plugins/pr-review-toolkit/) | Command | 6-agent PR review specialization (`/pr-review-toolkit:review-pr`) |
| [**ralph-wiggum**](./plugins/ralph-wiggum/) | Command | Self-referential AI loops for iterative development (`/ralph-loop`) |
| [**security-guidance**](./plugins/security-guidance/) | Hook | PreToolUse hook that monitors 9 common security patterns |

### Installing a plugin

```bash
# Copy any plugin folder into your project
cp -r plugins/code-review /path/to/your/project/.claude-plugin/
```

---

## 📝 Custom Commands

Located in [`.claude/commands/`](./.claude/commands/):

| Command | Purpose |
|---|---|
| `/commit-push-pr` | Automates commit → push → PR creation |
| `/dedupe` | Deduplication helper |
| `/oncall-triage` | On-call issue triage workflow |

---

## 🐳 DevContainer Setup (Windows)

[`scripts/run_devcontainer_claude_code.ps1`](./scripts/run_devcontainer_claude_code.ps1) automates DevContainer initialization with Docker or Podman on Windows.

```powershell
# Docker backend
.\scripts\run_devcontainer_claude_code.ps1 -Backend docker

# Podman backend
.\scripts\run_devcontainer_claude_code.ps1 -Backend podman
```

---

## 🔧 GitHub Automation Scripts

Located in [`scripts/`](./scripts/):

| Script | Purpose |
|---|---|
| `auto-close-duplicates.ts` | Bun script that auto-closes duplicate GitHub issues |
| `backfill-duplicate-comments.ts` | Backfills duplicate detection comments on existing issues |
| `comment-on-duplicates.sh` | Shell script for commenting on duplicate issues |

---

## Getting Started (Official Claude Code)

1. Install Claude Code:

   **macOS / Linux (Recommended):**
   ```bash
   curl -fsSL https://claude.ai/install.sh | bash
   ```

   **Homebrew:**
   ```bash
   brew install --cask claude-code
   ```

   **Windows (Recommended):**
   ```powershell
   irm https://claude.ai/install.ps1 | iex
   ```

   **WinGet:**
   ```powershell
   winget install Anthropic.ClaudeCode
   ```

2. Navigate to your project directory and run `claude`.

For full installation options, see the [official documentation](https://code.claude.com/docs/en/overview).

---

## Reporting Bugs

- **Claude Code bugs** → use `/bug` in Claude Code or file an issue at [anthropics/claude-code](https://github.com/anthropics/claude-code/issues)
- **Plugin bugs in this fork** → open an issue here

## Connect on Discord

Join the [Claude Developers Discord](https://anthropic.com/discord) to connect with other Claude Code users.
