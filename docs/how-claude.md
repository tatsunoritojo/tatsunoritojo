# How Claude Code works here

![How Claude Code works here diagram](../assets/diagrams/how-claude-v4.png)

Claude Code is the **implementer in the repository**—not the product owner.

This page is the prose companion to the diagram on my [GitHub profile](https://github.com/tatsunoritojo).  
**日本語:** [How Claude Code works here（日本語）](./ja/how-claude.md)  
Related: [How I ship](./how-i-ship.md) · [How knowledge compounds](./how-knowledge.md)

---

## Role split

| Claude Code **reads** | Claude Code **does** | Claude Code **does not own** |
|------------------------|----------------------|------------------------------|
| Issue · acceptance | Scoped branch changes | Product scope |
| Project rules · relevant docs | Tests · build | Review judgment |
| | | **Merge to main** |

Hands-on verification is not claimed as Claude-only; the diagram lists automated checks Claude typically runs. Human hands-on still happens when the change needs it.

---

## After implement (same order as How I ship)

Aligned with the full ship loop—not a shortcut that skips gates.

1. **Codex review**  
   Adversarial review against Issue scope. Findings are candidates.

2. **Human judgment**  
   I keep or reject findings. Claude does not decide which review notes stick.

3. **Open PR (Claude Code)**  
   Claude opens the PR, links the Issue, and records decisions.  
   Opening a PR is **not** the same as merging.

4. **I merge (human gate only)**  
   Merge to main is mine. ChatGPT may assist discussion; the merge decision is human.

---

## Why this shape

- **Avoids “AI shipped it” theater.** Implementation help without ownership of scope or merge.
- **Matches private product practice** where the human is the brain (decisions, merge) and Claude is the programmer (branch, PR), with adversarial review before PR.
- **Stays shorter than How I ship** on purpose: this page is about Claude’s boundary, not the full multi-tool story.

---

## What this is not

- Not “Claude Code merges for me.”
- Not “Claude owns the product roadmap.”
- Not a full substitute for [How I ship](./how-i-ship.md) (frame, Issue control, production, revise paths).

---

## Cross-links

| If you want… | Read |
|--------------|------|
| Full multi-tool loop | [How I ship](./how-i-ship.md) |
| Where claims and Issues come from | [How knowledge compounds](./how-knowledge.md) |
