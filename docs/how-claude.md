# How Claude Code works here

![How Claude Code works here diagram](../assets/diagrams/how-claude-v4.png)

## What this page is

This page explains **what Claude Code is allowed to do in my repos**—and what it is **not** allowed to own.

In short:

- Claude Code is an **implementer**, not the product owner.
- It **reads** Issues and docs, then **changes code on a branch**.
- It may **open a PR**.
- It does **not** decide product scope, final review judgment, or **merge to main**.

**日本語:** [How Claude Code works here（日本語）](./ja/how-claude.md)

Also:

- [How I ship](./how-i-ship.md) — full multi-tool loop from idea to production  
- [How knowledge compounds](./how-knowledge.md) — where claims and Issues come from  

---

## Who this is for

| Reader | What you should get |
|--------|---------------------|
| Profile visitor | Claude is not “shipping for me” unsupervised |
| Collaborator | Who opens the PR vs who merges |
| Future me | The boundary I keep |

---

## Role split (top of the diagram)

| **Reads** | **Does** | **Does not own** |
|-----------|----------|------------------|
| Issue · acceptance | Scoped branch changes | Product scope |
| Project rules · docs | Tests · build | Review judgment |
| | | **Merge to main** |

Notes:

- “Tests · build” are checks Claude typically runs.  
- **Hands-on** verification is not claimed as Claude-only; I still do it when the change needs a human eye.

---

## After implement (bottom of the diagram)

Same order as [How I ship](./how-i-ship.md)—gates are not skipped.

| Step | Who | What happens |
|------|-----|----------------|
| 1. Codex review | Codex | Hard review against the Issue |
| 2. Human judgment | Me | I keep or drop findings |
| 3. Open PR | **Claude Code** | Opens the PR, links the Issue |
| 4. I merge | **Me only** | Merge to main (or send back) |

Important:

| Action | Owner |
|--------|--------|
| Open PR | Claude Code |
| Merge | Human (me) |

Opening a PR is **not** the same as merging.

---

## How this fits the other two pages

| Page | Focus |
|------|--------|
| [How knowledge](./how-knowledge.md) | Observation → claim → Issue |
| [How I ship](./how-i-ship.md) | Full path including ChatGPT, loops, production |
| **This page** | Claude’s **boundary** only (shorter on purpose) |

---

## What this is not

- Not “Claude Code merges for me”
- Not “Claude owns the roadmap”
- Not a full substitute for [How I ship](./how-i-ship.md)

---

## Links

- [How I ship](./how-i-ship.md)  
- [How knowledge compounds](./how-knowledge.md)  
- Profile: [tatsunoritojo](https://github.com/tatsunoritojo)
