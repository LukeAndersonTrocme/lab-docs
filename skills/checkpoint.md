# Checkpoint

## Overview

Write a structured checkpoint document from the current session. The checkpoint is human-readable and doubles as a full context-setter for resuming work in a new Claude Code session. Always writes the same rich structure.

## When to Use

- "I'm done for now" — stepping away, want to resume later
- "Let me capture this before continuing" — milestone reached mid-session
- "This conversation is getting long" — want a clean handoff before starting fresh

**This is not a luke-check.** The `/luke-check` skill asks whether you are still thinking for yourself — it is a mid-session reflection tool. This skill documents what happened so you can pick it up again later.

---

## Workflow

### Step 1 — Extract from conversation

Read the full conversation and extract:
- What was worked on and what was produced
- Decisions made and the reasoning behind them
- Files created, modified, or referenced
- What is unresolved or outstanding

### Step 2 — Infer location and confirm

Propose a save path and wait for confirmation before writing.

**Location logic (in order of preference):**

1. **Git repo** — if the work is in a git repo, suggest saving to `docs/` or a `notes/` folder within it
2. **Project folder** — if there is a clear project folder, save there
3. **No obvious location** — ask: "Where should I save this checkpoint?"

**Filename:** `checkpoint_YYYY-MM-DD.md`. If a checkpoint for today already exists at that path, append `-2`, `-3`, etc.

**Confirmation:** Use the `AskUserQuestion` tool — do not ask via plain text. Propose the path and offer two options: confirm or change location. Do not write anything until the path is confirmed.

### Step 3 — Write the checkpoint

Write the full document in one shot.

---

## Structure

Every checkpoint has all six sections, in this order.

### Title block

```markdown
# Checkpoint — [Short Description of Session]
**Date:** YYYY-MM-DD
**Session scope:** [One sentence: what this session was about]
```

### 1. What Was Accomplished

Concrete and specific. Not "worked on the analysis" — "rewrote the pedigree filtering function; reduced runtime from 4 min to 40 sec on the test dataset." Include script names, file paths, numbers, outcomes. Use subheadings if multiple workstreams.

### 2. Key Decisions Made

What was decided and *why*. If the reasoning was not stated explicitly in the conversation, note that. Bullet list. This is what makes the checkpoint useful weeks later.

### 3. Files Created / Modified

Table of paths and status. Omit this section entirely if no files were created or modified.

```markdown
| File | Status |
|------|--------|
| `src/filter_pedigrees.py` | Created |
| `analysis/main.py` | Modified |
```

### 4. Next Steps

Checkbox list ordered by urgency. Include real dates where known.

```markdown
- [ ] **Most urgent thing** — due YYYY-MM-DD
- [ ] Second priority
- [ ] Lower priority item
```

### 5. Open Questions

Unresolved strategic or technical questions that surfaced in the session. Numbered list. Omit if none.

### 6. How to Continue in a New Session

Three subsections, always present:

**Files to read first** — ordered list, most important first. Infer from what was actively used or referenced in the conversation. Always include this checkpoint file itself last.

**Project context** — 2–4 sentences written for a reader with zero memory of this conversation. Background on the *project*, not this session: what it is, what stage it is at, what constraints matter.

**Working notes** — only include if something about your working context or preferences was specifically relevant in this session and would help a new instance hit the ground running. Omit if nothing notable.

---

## Quality Check

Before finalizing:
- [ ] All six sections present (even if some are brief)
- [ ] "What was accomplished" is specific — no generic phrases
- [ ] "Key decisions" captures reasoning, not just outcomes
- [ ] "Files to read first" reflects what was actually used
- [ ] "Project context" reads correctly to someone with no memory of this session
- [ ] Save path confirmed before writing
- [ ] Filename follows `checkpoint_YYYY-MM-DD.md` convention
