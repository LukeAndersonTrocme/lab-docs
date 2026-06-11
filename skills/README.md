# Lab Skills

These skills extend Claude Code with structured workflows for the lab's research context. Install them alongside [Superpowers](https://github.com/obra/superpowers) and [ECC](https://github.com/affaan-m/ECC).

## Installation

Copy the `.md` files from this folder into your Claude skills directory — typically `~/.claude/skills/`. You can create that directory if it does not exist.

```bash
mkdir -p ~/.claude/skills
cp skills/*.md ~/.claude/skills/
```

Then invoke any skill from within a Claude Code session with `/skill-name`.

## Available Skills

| Skill | Invocation | When to use |
|-------|------------|-------------|
| [Luke Check](luke-check.md) | `/luke-check` | Mid-session — pause and check that you are still thinking for yourself |
| [Checkpoint](checkpoint.md) | `/checkpoint` | End of session — document your work and set up a clean handoff for resuming later |

See the [AI tools guide](../ai-tools/README.md) for guidance on when and how to use each skill.
