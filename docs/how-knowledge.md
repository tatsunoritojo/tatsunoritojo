# How knowledge compounds

![How knowledge compounds diagram](../assets/diagrams/how-knowledge-v2.png)

Chat is draft. Claims need evidence. Outcomes decide what survives.

This page is the prose companion to the diagram on my [GitHub profile](https://github.com/tatsunoritojo). Related: [How I ship](./how-i-ship.md) · [How Claude Code works here](./how-claude.md)

---

## Where things live

| Home | Role |
|------|------|
| **Obsidian** | Claims, judgment notes, research capture—the “second brain” layer |
| **repo docs / ADR** | Decisions that affect a **product**—when it becomes shared truth in the repository |
| **GitHub Issue** | Scopes the **change** (acceptance criteria, one unit of work) |

I do **not** claim that all knowledge lives in Obsidian, or that every repo is a full SSOT for everything. Placement depends on whether the thing is personal judgment, product decision, or implementable change.

---

## Stages

### CAPTURE (vault)

1. **Observe evidence**  
   Research, field feedback, review notes, production incidents, user reactions—anything worth not losing.

2. **Normalize a claim** → **Obsidian**  
   Turn observation into a claim with evidence, intended use, and risk.  
   This is where fuzzy chat becomes something I can revisit.

### DECIDE (docs then Issue)

3. **Record decision context** → **repo** (when product is affected)  
   Docs and ADRs when the decision will outlive the chat and affect how software is built.  
   Personal notes may stay in the vault until they graduate.

4. **Define scope & acceptance** → **GitHub Issue**  
   Criteria, one change at a time.  
   Spec/docs and Issue stay separate: docs say *what is true*; Issue says *what we change next*.

### BUILD (repo)

5. **Implement on a branch**  
   Scoped changes. Detail of tools and gates: [How I ship](./how-i-ship.md).

6. **Verify behavior**  
   Tests, build, and hands-on checks as appropriate—not “green CI only.”

### LEARN (back to vault)

7. **Evaluate the outcome**  
   Promote, revise, or reject what we believed.  
   **learn → next claim (Obsidian):** not every outcome graduates; many claims get weakened or dropped.

---

## How this connects to shipping

Knowledge → Issue is how research becomes a controlled change.  
Shipping without a claim trail is how teams re-learn the same lesson.  
Claims without outcomes are just opinions with better formatting.

---

## What this is not

- Not “everything goes in the vault forever.”
- Not “chat history is the source of truth.”
- Not a replacement for [How I ship](./how-i-ship.md)—this is the longer arc *around* a change.
