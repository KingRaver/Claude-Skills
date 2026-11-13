# claude-skills

```
  ██████╗██╗      █████╗ ██╗   ██╗██████╗ ███████╗    ███████╗██╗  ██╗██╗██╗     ██╗     ███████╗
 ██╔════╝██║     ██╔══██╗██║   ██║██╔══██╗██╔════╝    ██╔════╝██║ ██╔╝██║██║     ██║     ██╔════╝
 ██║     ██║     ███████║██║   ██║██║  ██║█████╗      ███████╗█████╔╝ ██║██║     ██║     ███████╗
 ██║     ██║     ██╔══██║██║   ██║██║  ██║██╔══╝      ╚════██║██╔═██╗ ██║██║     ██║     ╚════██║
 ╚██████╗███████╗██║  ██║╚██████╔╝██████╔╝███████╗    ███████║██║  ██╗██║███████╗███████╗███████║
  ╚═════╝╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚═════╝ ╚══════╝    ╚══════╝╚═╝  ╚═╝╚═╝╚══════╝╚══════╝╚══════╝
```

> **A personal library of Claude Code skills** — packaged expertise that drops into Claude's context and transforms it from a general assistant into a specialist that already knows what you're building, how you like to build it, and exactly what "done" looks like.

---

## What is a `.skill` file?

A `.skill` file is a self-contained knowledge capsule for Claude Code. Each one bundles:

- A **trigger description** — tells Claude when to activate the skill automatically
- **Reference material** — patterns, token systems, architecture guides, implementation blueprints
- **Opinionated defaults** — so you never have to repeat yourself

Drop a `.skill` into Claude Code and it learns a new domain. Permanently.

---

## Skills in this library

### Infrastructure & Auth

| Skill | What it does |
|---|---|
| `2fa-totp.skill` | Adds production-grade TOTP two-factor authentication to an existing Turborepo monorepo — QR codes, backup codes, session invalidation, the full stack |
| `monorepo-migration.skill` | Takes two separate live repos and merges them into a clean Turborepo monorepo with shared packages, unified CI, and zero breakage |

### Frontend

| Skill | What it does |
|---|---|
| `professional-frontend.skill` | Interview-led UI design: runs a design discovery interview, derives a project-specific contrast-validated palette and token set, then builds consistent product UI. Outputs HTML/CSS and React/JSX |
| `frontend-upgrade.skill` | Audits and improves an *existing* Next.js / React codebase across three axes: mobile responsiveness, visual design, and interactivity |
| `elite-react-ui-architect.skill` | Crafts production-ready React UI with TailwindCSS, shadcn/ui and Framer Motion — dashboards, landing pages, glassmorphism and micro-interactions at Stripe / Linear / Vercel polish |
| `brand-identity.skill` | Develops a project's brand identity through an interview and three distinct concepts, then builds the logo mark, wordmark and full favicon / app-icon set |
| `eu-cookie-compliance.skill` | Implements full EU cookie consent under ePrivacy Directive and GDPR — banner logic, consent storage, per-category opt-in/out |

### AI & Agents

| Skill | What it does |
|---|---|
| `messaging-agent.skill` | Builds a deployable Claude-powered agent that lives inside Telegram (or Slack / Discord) and deeply understands your app's workflows |
| `x402-pos-terminal.skill` | Builds a mobile-optimised x402 crypto payment point-of-sale terminal |

### Project Intelligence

| Skill | What it does |
|---|---|
| `project-advisor.skill` | Deep-researches a GitHub repo and produces a prioritised improvement report — feature gaps, architecture, DX, docs |
| `project-builder.skill` | Drives an existing project through three phases: **Scaffold → Review → Execute** |
| `project-scaffold.skill` | Takes an idea through brainstorm and clarifying questions to a starting doc set (spec, structure, README, changelog, `CLAUDE.md`, style guide) and a question-based folder layout — asks which files to write, where they go, and how to handle existing ones |
| `project-workshop.skill` | Full lifecycle skill — raw idea through spec, docs, build plan, code review, and active improvement |
| `doc-feature-extractor.skill` | Reverse-engineers a product's integration surface from its developer docs, then maps it to implementation patterns |
| `gaps.skill` | Deep-dives a codebase for feature gaps and security vulnerabilities, then produces a phased, actionable checklist |
| `enterprise-features.skill` | Deep-dives a campaign / bulk-email product's codebase as a corporate executive assistant to produce an enterprise feature plan. Set the product name and file paths in its Configuration section |
| `docs-reorg.skill` | Restructures a repo's docs into purpose-named folders (`plans/`, `audits/`, `guides/`, `specs/`, …) — audits docs against code, then runs an operator-approved plan. Nothing is deleted |
| `project-archaeology.skill` | Reverse-engineers an existing codebase and its git history (original core vs. later additions) into an as-built dossier, a rebuild spec, and the project's documentation foundation |

### Build & Ship

| Skill | What it does |
|---|---|
| `phase-runner.skill` | Executes **one** phase of a phased checklist doc (`SCAFFOLDING.md`, `REVIEW_SCAFFOLDING.md`, `ROADMAP.md` — whatever you point it at), verifies with the repo's real lint / typecheck / build / test commands, and only ticks items off once they actually pass |
| `next-work.skill` | Starts the next piece of work from a fresh `main` — fetches, fast-forwards or flags divergence, then asks what's next and suggests branch names before branching |
| `ship.skill` | The full finish-and-land cadence for completed work: verify → docs → changelog → commit → PR to main, with git guardrails and a hard stop on any red step |
| `simple-pr.skill` | The minimal cadence — branch → commit → changelog (only if one exists) → push → PR. No verification gate, for changes that don't need one |

### Compliance

| Skill | What it does |
|---|---|
| `compliance-suite.skill` | Runs the statutory audit system end-to-end: shared intake → applicability triage → regime agents → synthesis. ISO 27001 and SOC 2 are elective and invoked directly alongside it |
| `compliance-synthesis.skill` | Merges the regime and attestation-framework audits into one cross-regime report — deduplicates findings so one fix satisfies many obligations |
| `mica-compliance.skill` | Audits a crypto-asset service provider's codebase against MiCA's code-level obligations, including the ICT/DORA and travel-rule controls |
| `gdpr-compliance.skill` | Audits a product against GDPR's code-level obligations — lawful basis, data-subject rights, security of processing, breach notification, transfers |
| `nis2-compliance.skill` | Audits a product against NIS2, validating the governing member-state law first, then the Art. 21 measures and Art. 23 reporting timelines |
| `dora-compliance.skill` | Audits a financial entity's code across all five DORA pillars: ICT risk, incidents, resilience testing / TLPT, third-party risk, information sharing |
| `iso27001-compliance.skill` | ISO/IEC 27001:2022 certification-readiness audit — ISMS scope and Statement of Applicability first, then the Annex A controls with a code surface |
| `soc2-compliance.skill` | SOC 2 readiness audit against the AICPA Trust Services Criteria, stating the Type I / Type II boundary explicitly |

### Skill Tooling

| Skill | What it does |
|---|---|
| `skill-creator.skill` | Creates, edits, optimizes and evals/benchmarks skills. Assumes a local-plugin marketplace; set the plugins root and marketplace name in its Configuration section on first use |

---

## How skills activate

Skills are loaded into Claude Code via the CLI. Once active, they trigger automatically based on what you're building — no manual invocation needed for most cases.

```bash
# List available skills
claude skills list

# Activate a skill for the current project
claude skills use professional-frontend
```

Claude reads the trigger descriptions and activates the right skill when it recognises the context. You can also invoke them explicitly with a slash command:

```
/professional-frontend  →  builds a polished UI from your brief
/project-advisor        →  audits a GitHub repo URL you provide
/messaging-agent        →  scaffolds a Telegram bot for your app
/phase-runner           →  implements one phase of your build plan
/ship                   →  verifies, documents, and opens the PR
```

---

## Design philosophy

**Skills are opinions, not options.**
Each skill encodes a specific point of view on how something should be built — which libraries, which patterns, which tradeoffs. This means less decision fatigue and faster time-to-shipped.

**Skills compose.**
`project-scaffold` → `project-builder` → `project-workshop` forms a complete project lifecycle, and `phase-runner` → `ship` closes the loop by executing the plan those skills write and landing it. `professional-frontend` pairs naturally with `eu-cookie-compliance`. Stack them.

**Skills are alive.**
As patterns evolve, skills get updated. The `.skill` format bundles reference docs alongside the trigger logic, so Claude always has current context — not a frozen snapshot.

---

## Repo structure

```
claude-skills/
├── 2fa-totp.skill               # TOTP 2FA implementation
├── brand-identity.skill         # Logo, wordmark, favicon set
├── compliance-suite.skill       # End-to-end EU compliance run
├── compliance-synthesis.skill   # Cross-regime compliance report
├── doc-feature-extractor.skill  # Docs → feature map
├── docs-reorg.skill             # Docs restructure by purpose
├── dora-compliance.skill        # DORA readiness audit
├── elite-react-ui-architect.skill # Polished React UI
├── enterprise-features.skill    # Campaign / bulk-email enterprise plan
├── eu-cookie-compliance.skill   # GDPR / ePrivacy consent
├── frontend-upgrade.skill       # Existing frontend improvement
├── gaps.skill                   # Feature + security gap audit
├── gdpr-compliance.skill        # GDPR readiness audit
├── iso27001-compliance.skill    # ISO 27001 readiness audit
├── messaging-agent.skill        # Telegram / Slack / Discord agent
├── mica-compliance.skill        # MiCA readiness audit
├── monorepo-migration.skill     # Turborepo consolidation
├── next-work.skill              # Fresh main → named branch
├── nis2-compliance.skill        # NIS2 readiness audit
├── phase-runner.skill           # Execute one phase of a build plan
├── professional-frontend.skill  # Design-system-first UI building
├── project-advisor.skill        # Repo audit & improvement report
├── project-archaeology.skill    # Codebase + history → rebuild spec
├── project-builder.skill        # Scaffold → Review → Execute
├── project-scaffold.skill       # Idea → project scaffold
├── project-workshop.skill       # Full project lifecycle
├── ship.skill                   # Verify → docs → changelog → PR
├── simple-pr.skill              # Branch → commit → PR, no gate
├── skill-creator.skill          # Create / eval skills
├── soc2-compliance.skill        # SOC 2 readiness audit
└── x402-pos-terminal.skill      # x402 crypto POS terminal
```

---

<div align="center">

Built for [Claude Code](https://claude.ai/code) · Maintained by [@KingRaver](https://github.com/KingRaver)

</div>
