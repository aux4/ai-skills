# ai skills list

```beforeAll
mkdir -p test-skills/my-skill
echo '---
name: my-skill
description: A test skill
---

# My Skill

Test instructions.' > test-skills/my-skill/SKILL.md
```

```afterAll
rm -rf test-skills
```

## should list installed skills

```timeout
30000
```

```execute
aux4 ai skills list --skillsDir test-skills
```

```expect:partial
my-skill
```
