# Using Claude AI in the Lab

The lab provides Claude Pro subscriptions and Claude Code access to all members. This guide describes how the PI uses these tools day-to-day and what has worked well for research workflows. It is a living document — if you discover something useful, please document it and share it with the lab.

---

## Philosophy

Claude is a thinking partner, not a co-author. At its best it accelerates the parts of your work that would otherwise be slow and mechanical: debugging code, drafting structure, generating alternative approaches, searching for the right framing. At its worst it generates plausible-sounding content you haven't thought through, or pulls you into a long session that felt productive but didn't advance your actual science.

The key is staying behind the steering wheel. Claude can suggest a route, help you navigate, and flag things you missed — but you choose the destination, and you are responsible for where you end up. If you could not explain the output to your supervisor or defend it to a peer, you are not ready to use it.

This matters especially in research. The hypothesis must be yours. The interpretation must be yours. The critical evaluation must be yours. Claude cannot replace that judgment, and you should not let it try.

---

## Getting Started

### 1. Claude Pro (Web)

You have been set up with a Claude Pro account at [claude.ai](https://claude.ai). Use your lab credentials. The web interface is good for writing, brainstorming, and conversations where you want a clean session without file access.

### 2. Claude Code (CLI + VSCode)

Claude Code is a command-line tool that integrates Claude directly into your coding environment. It is the primary recommended interface for any work that involves code or files. Install it from [claude.ai/code](https://claude.ai/code) and install the Claude Code extension for VSCode from the [VSCode Marketplace](https://marketplace.visualstudio.com/items?itemName=Anthropic.claude-code).

The VSCode integration lets Claude see your files, run commands, and work alongside you as you code — significantly more capable than the web interface for technical work. This also means you need to be intentional about what you approve. See [Safety and Permissions](#safety-and-permissions) below.

### 3. Installing Skills

Skills are structured workflows that let Claude follow a consistent, repeatable process for common tasks. The lab uses three sources:

- **[Superpowers](https://github.com/obra/superpowers)** — core research workflows: brainstorming, writing plans, executing plans. Follow the installation instructions in that repo.
- **[Everything Claude Code (ECC)](https://github.com/affaan-m/ECC)** — additional coding and productivity workflows. Follow the installation instructions in that repo.
- **This repository** (`skills/`) — lab-specific skills. Copy the `.md` files from `skills/` into your Claude skills directory (see [skills/README.md](../skills/README.md) for details).

---

## Primary Use Cases

### Code and Debugging

This is where Claude Code is most effective. Good uses:

- **Debugging** — describe the error and what you expected; Claude will often identify the issue and suggest a fix faster than searching Stack Overflow
- **Code review** — ask Claude to review a script before you commit; it will catch things you missed
- **Unfamiliar tools** — "how do I write this in Hail / pysam / R?" when you would otherwise spend 20 minutes searching documentation
- **Refactoring** — "this function is getting long; how should I break it up?"

Claude sometimes produces code that looks correct but has subtle bugs. Always test the output. If you do not understand a block of code Claude wrote, do not commit it — ask Claude to explain it line by line first.

### Brainstorming and Planning

Use the `/brainstorming` skill (from Superpowers) for any non-trivial new piece of work. It follows a structured process: understand the goal, explore approaches, present a design, write a spec, and only then move to implementation. This prevents spending a day building the wrong thing.

The `/fleshout` skill is useful for quick idea sprints — 10–15 minutes to develop a half-formed idea before the momentum fades. It works well immediately after a lab meeting or when something clicks during reading.

For larger development work, the full workflow is: `/brainstorming` → `/writing-plans` → `/executing-plans`. Each step hands off to the next with a clear artifact (spec, then plan, then implementation).

---

## What Not to Use it For

> **Do not submit sensitive project data to Claude or any AI tool.** This includes individual-level records, pedigrees, genomic data, or any data that must remain on the Alliance clusters.

Code and aggregate summary statistics are generally fine. When in doubt, ask the PI.

Full policy is in [Section 5 of the sensitive data guide](../data-management/sensitive-data-guide-en.md#5-ai-tools).

---

## Organizing Your Work with Claude

Claude can help you structure a project well from the start — file naming, folder hierarchies, documentation conventions. This is worth doing early, before a project grows into an unwieldy pile of files named `script_v2_FINAL_revised.py`.

**Use git.** Before any Claude Code session where files will be modified, make sure your working directory is a git repo with no uncommitted changes. Commit frequently during the session. This gives you a clear record of what Claude changed and makes it trivial to revert anything you did not intend. If you are not yet in the habit of using git, now is the time to start — Claude can help you learn it.

**Ask Claude to design the structure first.** Before writing code, ask: "How should I organize this project?" A few minutes here saves significant reorganization later.

**Push to GitHub.** Keep a remote copy of your work. This is not just for backup — it also makes it easy to share work with the PI and to collaborate. Claude can help you set up a repo and write a useful README.

**Use meaningful names.** Claude can help you develop naming conventions for files, variables, and directories that will still make sense six months from now. Ask it to propose a convention before you start generating outputs.

---

## Safety and Permissions

Claude Code runs on your machine and can read files, write files, and execute commands. When it asks to do something, you will see a permission prompt.

**Read the prompt before approving.** Things to watch:

- **File modifications** — Claude can and will edit files. Keep git commits frequent so you can see exactly what changed and revert easily.
- **Command execution** — Claude may suggest running shell commands, installing packages, or modifying configuration. Understand the command before approving.
- **Network access** — Claude can make network requests. Be aware of what it is accessing, particularly if you are working near any sensitive files.
- **Never use `--dangerously-skip-permissions`** unless you fully understand the context. This flag disables all permission prompts.

If something Claude did surprises you, stop the session. Run `git diff` to review all changes, and `git checkout` to revert anything you do not want. This is exactly why frequent commits matter.

---

## Lab Skills

Two skills are included in the `skills/` folder of this repository:

**[`/luke-check`](../skills/luke-check.md)** — A mid-session reflection to make sure you are still thinking for yourself. Run it when you have been in a Claude session for a while, or before committing and presenting Claude-assisted work. Think of it as a quick "what would my supervisor say about this right now?" It takes about two minutes.

**[`/checkpoint`](../skills/checkpoint.md)** — An end-of-session documentation tool. Writes a structured summary of what you accomplished, what decisions were made, and how to resume the work in a new session. Run it before closing any session you will want to return to.

These serve different purposes and are meant to be used together: `luke-check` during a session, `checkpoint` at the end.

---

## Explore and Share

Claude is a rapidly evolving tool and the lab's practice with it is still developing. You are encouraged to explore beyond what is described here — follow UdeM's guidelines, do not use sensitive data, and use your judgment.

**If you find a workflow or use case that works well, please document it and share it with the lab.** Open a pull request against this repository with your additions, or bring it to the PI. The lab benefits collectively from each member's experience.

---

*Last updated: 2026-06-11. Maintained by the PI. Questions? Ask the PI.*
