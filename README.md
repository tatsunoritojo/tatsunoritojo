<!--
  Mobile-first profile surface:
  - one wide banner so Start here stays near first scroll
  - no multi-column galleries, no autoplay video
  Banner: assets/pin-banner.jpg (= variations/05-flat-split)
  Alts: assets/alt-01-geometric.jpg, assets/alt-07-washi-ink.jpg
  Claims (fact-checked with owner 2026-07-18 / 2026-07-19):
  - Onedrop: built attendance/ops systems — NOT the public school website (onedrop2025.com)
  - Kodomo Shinro pair: commissioned by Onedrop — site + diagnostic (2 products)
  - Dev loop (Codex-reviewed 2026-07-19, VERDICT request-changes applied):
    Frame → Define Issue/docs/acceptance → Implement (Claude Code) → Verify → Codex review → Human judgment → PR → Human merge gate (ChatGPT assists; I merge/revise)
  - Evidence: onedrop/WORKFLOW.md; 260719_how_i_ship_codex_review.md
  - Knowledge axis (public-safe): research→claim→spec/ADR→implement→outcome; second brain + per-repo SSOT; Claude Code = implementer not owner (WORKFLOW 3-actor + vault claim protocol)
-->
<p align="center">
  <img src="assets/pin-banner.jpg" alt="From education into software" width="100%" />
</p>

<h1 align="center">Tatsunori Tojo</h1>

<p align="center">
  <strong>From education into software.</strong><br />
  I build tools for learning and everyday work — mostly on the web.
</p>

### Start here

- [Portfolio](https://tatsunoritojo.com) — selected work and writing
- [MacKairu](https://github.com/tatsunoritojo/MacKairu) — a resident mascot AI for macOS
- [Onedrop attendance & ops](https://tatsunoritojo.com/works/education-ops) — school operations systems (attendance and related tooling; not the public school website)
- [こどもの進路案内所](https://kodomo-shinro.jp) · [通信制高校診断](https://shindan.kodomo-shinro.jp/) — two sites built for Onedrop (parent guide + diagnostic)
- [あいプリントLab](https://hirodai-3d-aiprint.com/) — Hiroshima University 3D-printer circle site (redesign; accessibility-first)
- [シフリー](https://tatsunoritojo.com/works/shifree) — shift-scheduling SaaS for small teams (希望→確定→Google Calendar; code private)

### How I ship

```mermaid
flowchart TB
  subgraph PLAN
    A["1 Frame the change<br/>ChatGPT · options and constraints"]
    B["2 Define scope and acceptance<br/>Issue · docs · criteria"]
  end

  subgraph BUILD
    C["3 Implement on a branch<br/>Claude Code · scoped changes"]
    D["4 Verify behavior<br/>tests · build · hands-on"]
  end

  subgraph REVIEW
    E["5 Run adversarial review<br/>Codex · diff vs scope"]
    F["6 Apply human judgment<br/>I verify findings · keep or reject"]
  end

  subgraph SHIP
    G["7 Open the pull request<br/>link Issue · record decisions"]
    H["8 Human merge gate<br/>ChatGPT reviews · I merge or revise"]
  end

  A --> B --> C --> D --> E --> F --> G --> H
  H -. revise .-> B

  classDef human fill:#14532d,stroke:#166534,color:#f0fdf4
  classDef ai fill:#f0fdfa,stroke:#0f766e,color:#0f172a
  classDef work fill:#ffffff,stroke:#94a3b8,color:#0f172a
  class A,C,E ai
  class B,D,G work
  class F,H human
```

<p align="center"><sub>Tools propose and critique. I verify and decide.</sub></p>



### How knowledge compounds

Not a pile of chat logs. Research and field work are normalized before they touch code.

```mermaid
flowchart LR
  R["Observe<br/>research · field notes · review"]
  C["Claim<br/>evidence · use · risk · handoff"]
  S["Spec<br/>Issue · docs · ADR"]
  I["Implement<br/>branch · verify"]
  O["Outcome<br/>promote · revise · reject"]

  R --> C --> S --> I --> O
  O -. feeds next claim .-> C
```

<p align="center"><sub>Second brain for durable claims · per-repo docs/ADRs for product truth · chat is draft, not source of truth</sub></p>

### How Claude Code works here

Claude Code is the implementer in the repo — not the product owner.

```mermaid
flowchart TB
  subgraph INPUTS["What it reads"]
    I1["Issue + acceptance criteria"]
    I2["Project rules CLAUDE.md / AGENTS.md"]
    I3["Relevant specs and ADRs"]
    I4["Claims / handoff notes when needed"]
  end

  subgraph DOES["What it does"]
    D1["Scoped changes on a feature branch"]
    D2["Tests · build · hands-on checks"]
    D3["Open PR with decision notes"]
  end

  subgraph DOES_NOT["What it does not do alone"]
    N1["Decide product scope"]
    N2["Merge to main / master"]
    N3["Skip Codex or human review"]
  end

  INPUTS --> DOES
  DOES --> X["Codex adversarial review"]
  X --> H["I keep or reject findings"]
  H --> P["PR · then human merge gate"]

  classDef no fill:#fef2f2,stroke:#f87171,color:#0f172a
  class N1,N2,N3 no
```

<p align="center"><sub>Repeatable skills for git / deploy / UI checks · judgment and merge stay with me</sub></p>


<p align="center">
  <sub>Public experiments live in the pin below · more at <a href="https://github.com/tatsunoritojo/pin-only">pin-only</a></sub>
</p>
