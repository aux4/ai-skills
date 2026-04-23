# aux4/ai-skills

Install and manage AI agent skills from the open skills ecosystem ([skills.sh](https://skills.sh)). Skills are reusable instruction sets that enhance AI agents with procedural knowledge, packaged as `SKILL.md` files following the Open Agent Skills specification.

This package wraps the `skills` CLI to integrate with the aux4 ecosystem and installs skills into the `skills/` directory, compatible with `aux4/ai-agent`.

## Installation

```bash
aux4 aux4 pkger install aux4/ai-skills
```

Requires Node.js (for `npx`).

## Quick Start

```bash
# Search for available skills
aux4 ai skills find "code review"

# Install all skills from a repository
aux4 ai skills add vercel-labs/agent-skills

# Install a specific skill from a repository
aux4 ai skills add anthropics/skills@skill-creator

# List installed skills
aux4 ai skills list

# Use with aux4/ai-agent
aux4 ai agent ask "Review my code using the code-review skill"
```

## Commands

### aux4 ai skills add

Install a skill from a GitHub repository, URL, or local path into the `./skills/` directory.

```bash
aux4 ai skills add <source>
```

Sources can be:
- GitHub shorthand (all skills): `vercel-labs/agent-skills`
- GitHub shorthand (specific skill): `anthropics/skills@skill-creator`
- Full URL: `https://github.com/user/repo`
- Local path: `./my-local-skills`

```bash
aux4 ai skills add vercel-labs/agent-skills
aux4 ai skills add anthropics/skills@skill-creator
aux4 ai skills add ./my-local-skills
```

For more details see [aux4 ai skills add](./commands/ai/skills/add).

### aux4 ai skills remove

Remove an installed skill.

```bash
aux4 ai skills remove <name>
```

```bash
aux4 ai skills remove code-review
```

For more details see [aux4 ai skills remove](./commands/ai/skills/remove).

### aux4 ai skills list

List all installed skills in the skills directory.

```bash
aux4 ai skills list
```

For more details see [aux4 ai skills list](./commands/ai/skills/list).

### aux4 ai skills find

Search the skills registry for available skills.

```bash
aux4 ai skills find <query>
```

```bash
aux4 ai skills find "database migration"
```

For more details see [aux4 ai skills find](./commands/ai/skills/find).

### aux4 ai skills update

Update all installed skills to their latest versions.

```bash
aux4 ai skills update
```

For more details see [aux4 ai skills update](./commands/ai/skills/update).

### aux4 ai skills init

Create a new SKILL.md template in the current directory.

```bash
aux4 ai skills init <name>
```

```bash
aux4 ai skills init my-new-skill
```

For more details see [aux4 ai skills init](./commands/ai/skills/init).

## Skills Directory

Skills are installed into `./skills/`. This is compatible with `aux4/ai-agent`, which reads skills from the same directory.

```
my-project/
├── AGENTS.md
├── skills/
│   ├── code-review/
│   │   └── SKILL.md
│   ├── testing/
│   │   └── SKILL.md
│   └── deploy/
│       └── SKILL.md
└── config.yaml
```

## SKILL.md Format

Each skill is a directory containing a `SKILL.md` file with YAML frontmatter:

```yaml
---
name: code-review
description: Review code for bugs, style issues, and security vulnerabilities
---

# Code Review

Instructions for the agent on how to perform code reviews...
```

## License

This package is licensed under the Apache License.

See [LICENSE](./license) for details.
