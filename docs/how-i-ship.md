# How I ship

![How I ship diagram](../assets/diagrams/how-i-ship-v4.png)

## What this page is

This page explains **how I take a software change from idea to production** when I work with AI tools.

In short:

- I do **not** ask AI to “just ship it.”
- I cut work into **one GitHub Issue at a time**.
- AI tools **propose and review**.
- **I decide** what merges.

**日本語:** [How I ship（日本語）](./ja/how-i-ship.md)

Also on this profile:

- [How knowledge compounds](./how-knowledge.md) — how ideas become claims and Issues  
- [How Claude Code works here](./how-claude.md) — what Claude Code is allowed to do (and not do)

---

## Who this is for

| Reader | What you should get |
|--------|---------------------|
| Visitor to my profile | How AI fits into my shipping process (not magic) |
| Collaborator | Where Issue, PR, and merge sit |
| Future me | The loop I try to keep |

---

## The flow at a glance

| Phase | Steps | Purpose |
|-------|--------|---------|
| **Plan** | 1 → 2 | Decide *what* change, and write it as an Issue |
| **Build · review (loop)** | 3 → 4 → 5 | Implement, get hard review, decide revise or ready |
| **Ship** | 6 → 7 | Open PR, then **I** merge (or send back) |

```
idea → plan (Issue) → build/review loop → PR → I merge → production
                ↑______________revise_________________|
```

---

## Who does what

| Role | Who / tools | Job |
|------|-------------|-----|
| Explore | ChatGPT (connected to the real repository) | Wall-bounce design using live repo context—not free-floating chat |
| Scope | Me + **GitHub Issue** | Acceptance criteria; one change unit |
| Implement | **Claude Code** | Work on a branch; open the PR |
| Hard review | **Codex** | Challenge the diff against the Issue |
| Decide findings | **Me** | Keep or drop review comments |
| Merge | **Me** | Only I merge to main |

Diagram colors follow these roles.

---

## Steps (same as the diagram)

### Plan

1. **Frame the change** — ChatGPT  
   Explore the problem and options **with ChatGPT connected to the actual repository**, so the wall-bounce is grounded in real code and project structure—not abstract advice.  
   This stage still produces options and questions, not a final contract.

2. **Define scope & acceptance** — me, GitHub Issue  
   Write what “done” means. Everything after is bound to this Issue.

### Build · review (loop)

3. **Implement** — Claude Code  
   Scoped work on a branch. No direct push to main.

4. **Adversarial review** — Codex  
   Review against Issue scope, not against “vibes.”

5. **Human judgment** — me  
   - **revise** → back to implement (same Issue)  
   - **ready** → leave the loop and open a PR

### Ship

6. **Open PR** — Claude Code  
   Link the Issue; record decisions (including rejected review notes).

7. **Human merge gate** — me  
   ChatGPT may help discuss the PR. **I merge** or send the work back to the Issue.  
   Then it can go to production.

---

## Feedback paths

| Path | When | Goes to |
|------|------|---------|
| **Loop revise** | Implementation or review is not good enough | Step 3 (implement), same Issue |
| **Issue revise** | Scope or acceptance is wrong | Step 2 (Issue) — do not restart from zero |

---

## What this is not

- Not “AI merges for me”
- Not one giant PR for a vague goal
- Not treating chat logs as the source of truth ([knowledge](./how-knowledge.md))

---

## Links

- Diagram on profile: [tatsunoritojo](https://github.com/tatsunoritojo)  
- [How knowledge compounds](./how-knowledge.md)  
- [How Claude Code works here](./how-claude.md)
