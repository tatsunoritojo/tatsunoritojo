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
  - Knowledge + Claude Code axis (Codex-reviewed 2026-07-19, request-changes applied): see 260719_profile_axis_codex_review.md
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

Useful observations become evidence-backed claims before they guide implementation.

```mermaid
flowchart TB
  A["Observe evidence<br/>research · field feedback · review"]
  B["Normalize a claim<br/>evidence · use · risk"]
  C["Record decision context<br/>docs · ADRs"]
  D["Define scope and acceptance<br/>Issue · criteria"]
  E["Implement on a branch<br/>scoped changes"]
  F["Verify behavior<br/>tests · build · hands-on"]
  G["Evaluate the outcome<br/>promote · revise · reject"]

  A --> B --> C --> D --> E --> F --> G
  G -. informs the next claim .-> B
```

<p align="center"><sub>Useful observations become evidence-backed claims; outcomes decide what survives. Decisions move into repository docs when they affect a product. Chat is draft, not source of truth.</sub></p>

### How Claude Code works here

Claude Code is the implementer in the repository — not the product owner.

| | |
|---|---|
| **Reads** | Issue, acceptance criteria, project rules, and relevant docs |
| **Does** | Implements scoped changes on a branch and runs available checks (`tests` · `build`) |
| **Does not own** | Product scope, review judgment, or the merge decision |

Then: **Codex** adversarial review → **I** keep or reject findings → **PR** → **human merge gate** (`I merge or revise`).

<p align="center"><sub>Claude Code implements scoped changes; I own product decisions, review judgment, and merge.</sub></p>


<p align="center">
  <sub>Public experiments live in the pin below · more at <a href="https://github.com/tatsunoritojo/pin-only">pin-only</a></sub>
</p>
