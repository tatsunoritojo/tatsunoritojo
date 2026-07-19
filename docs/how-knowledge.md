# How knowledge compounds

![How knowledge compounds diagram](../assets/diagrams/how-knowledge-v2.png)

## What this page is

This page explains **how I turn messy observations into something I can act on**—and when that becomes a software change.

In short:

- Chat is a **draft**, not the record of truth.
- I write **claims** with evidence (usually in **Obsidian**).
- Product decisions that must stick go into **repo docs / ADRs**.
- Work that will change code is cut as a **GitHub Issue**.
- After shipping, I **learn**—many claims get weaker or die.

**日本語:** [How knowledge compounds（日本語）](./ja/how-knowledge.md)

Also:

- [How I ship](./how-i-ship.md) — idea → production for one change  
- [How Claude Code works here](./how-claude.md) — implementer vs owner  

---

## Who this is for

| Reader | What you should get |
|--------|---------------------|
| Profile visitor | Why I separate “thinking,” “docs,” and “Issues” |
| Collaborator | Where to look for claims vs change tickets |
| Future me | Capture → decide → build → learn |

---

## Where things live (before the steps)

| Place | Use it for |
|-------|------------|
| **Obsidian** | Claims, judgment notes, research capture |
| **Repo docs / ADR** | Decisions that affect a **product** and should outlive chat |
| **GitHub Issue** | The **change** unit: scope and acceptance |

I do **not** say “everything is in Obsidian” or “every repo is the single source of truth for everything.”

---

## The flow at a glance

| Stage | Steps | Plain meaning |
|-------|--------|----------------|
| **Capture** | 1 → 2 | Notice something; write a claim you can revisit |
| **Decide** | 3 → 4 | If it matters for a product, document it; if we will change code, open an Issue |
| **Build** | 5 → 6 | Implement and check (see [How I ship](./how-i-ship.md)) |
| **Learn** | 7 → back to 2 | Did the claim hold? Update or drop it in the vault |

```
observe → claim (Obsidian) → docs/ADR if needed → Issue → build → evaluate
                ↑______________ learn (not every outcome graduates) ___|
```

---

## Steps (same as the diagram)

### Capture (vault)

1. **Observe evidence**  
   Research, field feedback, reviews, incidents, user reactions—anything worth not losing.

2. **Normalize a claim** → **Obsidian**  
   Turn the observation into a claim with evidence, intended use, and risk.

### Decide (docs, then Issue)

3. **Record decision context** → **repo** when a product is affected  
   Docs / ADRs when the decision must survive chat and guide how software is built.

4. **Define scope & acceptance** → **GitHub Issue**  
   What we change next, and how we know we’re done.  
   Docs say *what is true*; Issues say *what we change*.

### Build (repo)

5. **Implement on a branch**  
   Scoped changes. Tooling detail: [How I ship](./how-i-ship.md).

6. **Verify behavior**  
   Tests, build, and hands-on when needed—not “CI green only.”

### Learn (back to the vault)

7. **Evaluate the outcome**  
   Promote, revise, or reject what we believed.  
   **learn → next claim (Obsidian):** not every outcome becomes a stronger claim.

---

## How this connects to shipping

| Path | Meaning |
|------|---------|
| Knowledge → Issue | Research becomes a controlled change |
| Ship without claims | Easy to re-learn the same lesson |
| Claims without outcomes | Opinions with nicer formatting |

---

## What this is not

- Not “save everything in the vault forever”
- Not “chat history is the source of truth”
- Not a full replacement for [How I ship](./how-i-ship.md)—this is the longer arc *around* a change

---

## Links

- [How I ship](./how-i-ship.md)  
- [How Claude Code works here](./how-claude.md)  
- Profile: [tatsunoritojo](https://github.com/tatsunoritojo)
