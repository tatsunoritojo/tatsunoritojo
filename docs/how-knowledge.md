# How knowledge compounds

![How knowledge compounds diagram](../assets/diagrams/how-knowledge-v2.png)

[日本語](./ja/how-knowledge.md) · [How I ship](./how-i-ship.md) · [How Claude Code works here](./how-claude.md)

---

## What this page explains

This page explains **how I collect information, turn it into a revisit-able judgment, and only then open a software change** when one is needed.

If [How I ship](./how-i-ship.md) is “**one Issue through merge**,” this page is **before that Issue exists** and **after the outcome feeds the next judgment**.

| You will understand | You will not get |
|---------------------|------------------|
| What I gather and where it goes | Every tool’s setup manual |
| Why chat is not the source of truth | Every repo’s local rules |
| How learning updates (or kills) judgments | “AI organizes knowledge for free” |

In the diagram, “claim” means a **judgment with evidence and intended use**, something you can re-open later.

---

## Why information gathering comes first

If I jump to coding or to an Issue too early:

- I re-implement what already exists  
- I discover constraints (auth, PII, deadlines) too late  
- Wall-bounce becomes generic advice that does not fit *this* repository  

So the order is:

1. **Gather** — what is happening, what already exists  
2. **Write a judgment** — so it survives chat  
3. **Document** — if it changes how a product is built  
4. **Issue** — if we will change code  
5. **Build and check**  
6. **Learn** — update or drop the judgment  

---

## What I gather

| Kind | Examples | Why it matters |
|------|----------|----------------|
| Field / user | Support notes, stuck flows, manual ops | Grounds *what* to fix |
| Repo facts | Code paths, tests, config, docs | Grounds *where* to change |
| Past decisions | ADRs, old notes, incidents | Avoids re-litigating |
| External research | API behavior, library limits | Feasibility |
| Constraints | Deadlines, no-touch zones, security | Caps the scope |

### Where raw material goes

| Place | Good for | Bad for |
|-------|----------|---------|
| **Obsidian** | Research notes, hypotheses, personal judgment | Treating untested notes as product law |
| **Repo docs / ADR** | Product decisions others must follow | Unsorted scratch |
| **GitHub Issue** | One change unit + acceptance | Dumping entire research logs |

I do **not** put everything in one place. **Lifespan and audience** decide.

---

## Who this is for

| Reader | What you should get |
|--------|---------------------|
| Profile visitor | Why notes, docs, and Issues are separate |
| Collaborator | Where judgments live vs change tickets |
| Future me | Gather → judge → change → learn |

---

## Flow at a glance

| Stage | Steps | Plain meaning |
|-------|--------|----------------|
| **Capture** | 1 → 2 | Notice; write a judgment you can revisit |
| **Decide** | 3 → 4 | Product truth → docs; code change → Issue |
| **Build** | 5 → 6 | Implement and verify |
| **Learn** | 7 → 2 | Did the judgment hold? Update or drop it |

```
gather information → write judgment (Obsidian)
  → docs/ADR if product-affecting
  → GitHub Issue if we change code
  → implement & verify
  → evaluate (many judgments do not “graduate”)
```

---

## Steps in detail (1–7)

### 1. Observe evidence

**Goal:** Do not lose raw material that would cause rework later.

**Examples of practice:**

- Capture repro steps or screenshots  
- Light the likely code paths  
- Search similar past ADRs / Issues  
- Write down what is still unknown  

**Done when** facts and guesses are separated, and you can explain the situation to someone else with materials.

### 2. Normalize a judgment → Obsidian

**Goal:** Leave the chat stream and write something you can re-check.

| Element | Example |
|---------|---------|
| Assertion | “X is likely the cause / Y is the better approach” |
| Evidence | Logs, code refs, user reports |
| Use | What this is for (build, prioritize, keep researching) |
| Risk | What breaks if we are wrong |

**Done when** future-you can follow the evidence. This is Obsidian’s main job.

### 3. Record decision context → repo (when a product is affected)

**Goal:** Promote judgments that change **how the product is built** into shared docs / ADRs.

Stay in the vault when the idea is still untested scratch.

Do not merge “product law” and “next change ticket” into one blob.

### 4. Define scope & acceptance → GitHub Issue

**Goal:** Create the unit of code change that implement and review will share.

| | Docs / ADR | Issue |
|--|------------|--------|
| Role | What we treat as true | What we change *this time* |
| Lifespan | Long | For this change |
| Done | Policy remains written | Acceptance met and closed |

**Done when** [How I ship](./how-i-ship.md) step 2 could start from this Issue alone.

### 5. Implement on a branch

Shallow here. Tools and gates: [How I ship](./how-i-ship.md).  
Claude’s boundary: [How Claude Code works here](./how-claude.md).

### 6. Verify behavior

| Kind | Examples | Often who |
|------|----------|-----------|
| Automated | tests · build | Claude / CI |
| Hands-on | UI, real data, edges | Me when needed |

Green CI is necessary, not always sufficient.

### 7. Evaluate the outcome → learn back into Obsidian

| Outcome | What happens to the judgment |
|---------|------------------------------|
| As expected | Strengthen evidence or mark adopted |
| Partly wrong | Revise the hypothesis |
| Wrong | Drop it or return to observation |

The **learn → next claim** arrow is not “every story ends in success.” Most judgments get weaker or die.

---

## When to return to gathering

- Acceptance criteria will not write themselves (missing material)  
- Wall-bounce only returns generic advice (missing repo facts)  
- Review says the premise was wrong  

---

## Common failures

| Failure | Effect | Fix |
|---------|--------|-----|
| Only chat remains | Evidence evaporates | Write the judgment in Obsidian |
| Research dump in the Issue | Change unit unreadable | Issue = acceptance; research stays in vault |
| Docs ≡ Issue | Policy and work unit tangle | Keep them separate |
| No evaluation | Repeat the same judgment | Make step 7 habitual |

---

## How the three pages relate

| Page | Span |
|------|------|
| **This page** | Gather → judge → Issue → learn |
| [How I ship](./how-i-ship.md) | One Issue through merge |
| [How Claude Code works here](./how-claude.md) | Implementer boundary |

---

## Practice this page represents

Separate a research vault (Obsidian), product docs, and change Issues; update judgments after outcomes. Tool names may change. **Start with information gathering, and never treat chat as the source of truth.**
