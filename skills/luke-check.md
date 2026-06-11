# Luke Check

## Overview

A mid-session reflection to make sure you are still doing your own science. This skill asks four questions designed to catch the most common ways that AI-assisted work goes wrong. It takes about two minutes.

**This is not a checkpoint.** The `/checkpoint` skill documents your session for resumption later — it is an end-of-session tool. This skill is about the quality of your thinking *right now*. Use it mid-session, before you commit or present anything.

## When to Run It

- You have been in a Claude session for more than 30–45 minutes
- You are about to commit work or show it to someone
- Something feels slightly off but you cannot name what
- You notice you have been saying "yes" to everything Claude suggests

## The Four Questions

Claude will review what you have been working on and ask these questions in sequence. Answer honestly — even a brief internal answer counts.

### 1. Can you explain this in your own words?

Pick the most important thing Claude produced in this session: a block of code, an analysis approach, a written paragraph. Can you explain it to someone without referring to Claude's output? Could you reconstruct the reasoning from scratch if you had to?

*If the answer is no, you have not understood it yet. Do not move on until you do. Ask Claude to explain it to you — but the understanding must be yours before you proceed.*

### 2. Do you know what changed?

Run `git diff` or compare the current state to where you started. Do you know exactly what files were modified and why? Is there anything in the diff that surprises you?

*If there are surprises, stop and read them carefully before continuing. Never commit code you have not read. If you have not been committing as you go, this is a signal that the session has gotten away from you.*

### 3. Is this still your science?

Is the core direction — the hypothesis, the method, the interpretation — genuinely yours? Did you arrive at it through your own reasoning, with Claude helping you articulate or refine it? Or did Claude suggest it and you agreed without pushing back?

*It is fine to build on Claude's suggestions. It is not fine to accept them without evaluating them critically. Your name will be on this work.*

### 4. Are you still moving forward?

What was your original goal for this session? Are you closer to it? Or have you drifted into iterating prompts, exploring a tangent, or polishing something that does not need polish?

*If you have been "productive" for an hour but your actual goal has not moved, that is a rabbit hole. Name the original goal out loud. Ask whether the last hour served it.*

---

## After the Questions

If you answered yes to all four: good — keep going.

If you answered no to one: note it, address it, then continue.

If you answered no to two or more: stop. Commit what you have, close the session, and come back with fresh eyes. This is not failure — it is exactly what this check is for.

---

## How Claude Runs This Skill

When invoked, Claude will:

1. Briefly review what has been worked on in the current session
2. Ask the four questions in sequence, waiting for your response to each
3. Reflect back any concerns it notices — gently but honestly
4. Suggest whether to continue, pause and address something, or end the session with a `/checkpoint`
