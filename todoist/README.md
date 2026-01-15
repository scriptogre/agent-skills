# Todoist

Manage Todoist programmatically via its API.

---

## Setup

### 1. Get your Todoist API token

Todoist → Settings → Integrations → Developer → Copy API token

### 2. Configure the token (choose one method)

**Option A: Claude Code settings (recommended)**

Add to `~/.claude/settings.json`:

```json
{
  "env": {
    "TODOIST_API_TOKEN": "your_token_here"
  }
}
```

Available to all Claude Code sessions without exposing credentials in chat.

**Option B: Shell profile**

Add to `~/.zshrc` or `~/.bashrc`:

```bash
export TODOIST_API_TOKEN="your_token_here"
```

Then: `source ~/.zshrc`

**Option C: Project .env file**

Create `.env` in your project root:

```
TODOIST_API_TOKEN=your_token_here
```

Then load it when starting your session. ⚠️ Never commit this file.

### 3. Use the skill

Start your agent and tell it to read `SKILL.md`, or copy this skill to `~/.claude/skills/` for auto-discovery.

---

## What You Can Do

- List, create, update, and delete tasks
- Organize tasks into sections and projects
- Move tasks between sections (requires Sync API)
- Batch multiple operations in one request
- Convert task hierarchies into proper sections
