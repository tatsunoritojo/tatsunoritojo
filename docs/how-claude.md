# How Claude Code works here

![How Claude Code works here diagram](../assets/diagrams/how-claude-v4.png)


[日本語](./ja/how-claude.md) · [How I ship](./how-i-ship.md) · [How knowledge compounds](./how-knowledge.md)

---

## What this page explains

This page explains **what Claude Code is allowed to read, what it may do, and what it must never own** in my repositories.

It is a **zoom-in on the implementer boundary** inside [How I ship](./how-i-ship.md)—not a second full shipping guide.

| You will understand | You will not get here |
|---------------------|------------------------|
| What Claude reads as input | Full ChatGPT wall-bounce procedure |
| What diffs Claude may write | How product roadmap is set |
| Who opens the PR vs who merges | Every repo’s CI config |

---

## Prerequisite: information and an Issue first

Before Claude works, I want:

1. **Information gathering** (current code, constraints, trigger) — see [How knowledge compounds](./how-knowledge.md) and the start of [How I ship](./how-i-ship.md)  
2. A **GitHub Issue** with scope and acceptance  
3. **Docs / ADRs** when product decisions apply  

I do not hand Claude only “make it good.”  
**Implementation without readable material is fast and often wrong.**

---

## Role split (top of the diagram)

### READS

| Input | Why |
|-------|-----|
| GitHub Issue | Binding scope and acceptance |
| Project rules (e.g. CLAUDE.md) | Local prohibitions and procedure |
| Related docs / ADRs | Spec basis |
| Existing code | Footing for the change |

GitHub marks the Issue/repo surface.

### DOES

| Does | Does not |
|------|----------|
| Scoped changes on a dedicated branch | Direct push to main |
| Automated tests · build that apply | Drive-by refactors outside the Issue |
| Follow-up commits for review feedback | Silently rewriting acceptance |

**Hands-on** checks (UI, real data) are mine when the change needs them.  
Passing tests/build is not the same as “a human already tried it.”

### DOES NOT OWN

| Not owned by Claude | Owned by |
|---------------------|----------|
| Final product scope | Me (Issue / docs) |
| Review judgment (keep/drop findings) | Me |
| **Merge to main** | Me |

The dashed link from DOES is a **boundary**, not “next step in the pipeline.”

---

## After implement (bottom of the diagram)

Same order as [How I ship](./how-i-ship.md). Gates are not skipped.

| # | Step | Who | What |
|---|------|-----|------|
| 1 | Codex review | Codex | Stress-test the diff against the Issue |
| 2 | Human judgment | Me | Keep or reject findings |
| 3 | Open PR | **Claude Code** | Open PR, link Issue, record history |
| 4 | I merge | **Me only** | Merge to main or return to the Issue |

### Easy to confuse

| Action | Owner | Wrong reading |
|--------|--------|----------------|
| Open PR | Claude Code | “Humans do all PR work” |
| Merge | Human | “Claude merges” |

**Opening a PR is not merging.**

Codex findings are proposals. I check the real code; if I reject a finding, I leave a reason when it matters.

---

## Handoff in practice

```
[Gather info · wall-bounce · lock Issue]  ← me / ChatGPT / knowledge page
        ↓
[READS] Issue, docs, rules                 ← Claude
        ↓
[DOES] branch implement · tests/build      ← Claude
        ↓
[Codex] adversarial review
        ↓
[Me] keep or reject findings
        ↓
[Open PR] Claude opens the PR
        ↓
[I merge] I merge (or return to the Issue)
```

---

## Why split this way

1. **Speed vs responsibility** — Implementation can be fast; scope and merge stay human.  
2. **Reviews that matter** — Adversarial review + human acceptance prevents “rubber stamps.”  
3. **History** — Issue links, decisions, and rejections stay on the PR.

---

## Common misunderstandings

| Misunderstanding | Reality |
|------------------|---------|
| Claude sets the product | Scope is Issue / me |
| Claude merges | I merge |
| Automated tests finish the job | Hands-on when needed is mine |
| This diagram is the whole ship story | It is only Claude’s boundary |

---

## How the three pages relate

| Page | Role |
|------|------|
| [How knowledge compounds](./how-knowledge.md) | Gather → judgment → Issue |
| [How I ship](./how-i-ship.md) | Issue through merge (full tool cast) |
| **This page** | What Claude may read/write/never own |

---

## Practice this page represents

In private product work the skeleton matches: programmer = Claude Code (branch, PR), brain = me (decisions, merge), adversarial review before PR. CI and production steps differ by repository.
