# ai skills init

```afterAll
rm -rf test-skill
```

## should create a SKILL.md template

```timeout
30000
```

```execute
aux4 ai skills init test-skill
```

```execute
cat test-skill/SKILL.md
```

```expect:partial
name: test-skill
```

```expect:partial
description:
```
