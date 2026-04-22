#### Description

Install a skill from the open skills ecosystem into the local skills directory. Sources can be a GitHub shorthand (e.g., `vercel-labs/agent-skills`), a full Git URL, or a local path.

By default, skills are installed into `./skills/`, which is compatible with `aux4/ai-agent`. Override with `--skillsDir` to use a different directory.

#### Usage

```bash
aux4 ai skills add <source> [--skillsDir <path>]
```

source      Skill source — GitHub shorthand, URL, or local path (positional argument)
--skillsDir Directory to install skills into (default: skills)

#### Example

```bash
aux4 ai skills add vercel-labs/agent-skills
```

```bash
aux4 ai skills add ./my-local-skills --skillsDir ./custom-skills
```
