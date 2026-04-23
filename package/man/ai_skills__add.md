#### Description

Install a skill from the open skills ecosystem into the local `./skills/` directory. Sources can be a GitHub shorthand (e.g., `vercel-labs/agent-skills`), a full Git URL, or a local path. To install a specific skill from a multi-skill repository, use the `owner/repo@skill-name` format.

#### Usage

```bash
aux4 ai skills add <source>
```

source      Skill source — GitHub shorthand, URL, or local path (positional argument)

#### Example

```bash
aux4 ai skills add vercel-labs/agent-skills
```

```bash
aux4 ai skills add anthropics/skills@skill-creator
```

```bash
aux4 ai skills add ./my-local-skills
```
