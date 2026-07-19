# How I ship

![How I ship diagram](../assets/diagrams/how-i-ship-v4.png)

Not a one-shot magic button. One change at a time. Issue-scoped. Tools propose and critique; **I decide what ships.**

This page is the prose companion to the diagram on my [GitHub profile](https://github.com/tatsunoritojo).  
**日本語:** [How I ship（日本語）](./ja/how-i-ship.md)  
Related: [How knowledge compounds](./how-knowledge.md) · [How Claude Code works here](./how-claude.md)

---

## Roles (who does what)

| Role | Tools | Responsibility |
|------|--------|----------------|
| **Explore / critique** | ChatGPT, Codex | Wall-bounce design, adversarial review vs Issue scope |
| **Implement** | Claude Code | Branch work, open PR, record decisions in the PR |
| **Control plane** | GitHub Issue | Scope, acceptance criteria, one change unit |
| **Decide** | Human (me) | Keep or reject review findings; merge or send back |

Color on the diagram maps to these roles, not to “AI good / human bad.”

---

## Steps

### PLAN

1. **Frame the change (ChatGPT)**  
   Explore the problem, options, and rough design. This is conversation, not a contract.

2. **Define scope & acceptance (me · GitHub Issue)**  
   Cut the work into one Issue: acceptance criteria, docs links, what “done” means.  
   This is the control plane for everything after.

### BUILD · REVIEW (loop)

3. **Implement (Claude Code)**  
   Scoped changes on a dedicated branch. No direct push to main.

4. **Adversarial review (Codex)**  
   Review against the Issue scope—not against vibes. Findings are candidates, not orders.

5. **Human judgment (me)**  
   I keep or reject each finding.  
   - **revise** → back to implement (same Issue)  
   - **ready** → leave the loop and open a PR

### SHIP

6. **Open PR (Claude Code)**  
   Link the Issue, record decisions (including which Codex notes were rejected and why).

7. **Human merge gate (me)**  
   ChatGPT may assist with review discussion. **I merge** (or send back to the Issue).  
   Then the change can go to production.

### Feedback paths

- **Loop revise:** judgment → implement (still on the same Issue).  
- **Issue revise:** merge gate → Issue (scope or acceptance needs to change—don’t restart the universe).

---

## What this is not

- Not “AI merges for me.”
- Not one giant PR for a vague goal.
- Not treating chat logs as the source of truth (see [knowledge](./how-knowledge.md)).

---

## Evidence / practice

The same shape shows up in private product work (e.g. Issue → branch → PR → human merge, with adversarial review before PR). Details vary by repo; the public diagram is the portable version.
