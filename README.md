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
| `professional-frontend.skill` | Builds production-grade UIs using a strict design token system — spacing scale, typographic hierarchy, component consistency. Outputs HTML/CSS and React/JSX |
| `frontend-upgrade.skill` | Audits and improves an *existing* Next.js / React codebase across three axes: mobile responsiveness, visual design, and interactivity |
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
| `project-scaffold.skill` | Guides an idea through structured discovery and produces `SPEC.md`, `STRUCTURE.md`, and a ready-to-use project scaffold |
| `project-workshop.skill` | Full lifecycle skill — raw idea through spec, docs, build plan, code review, and active improvement |
| `doc-feature-extractor.skill` | Reverse-engineers a product's integration surface from its developer docs, then maps it to implementation patterns |

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
```

---

## Design philosophy

**Skills are opinions, not options.**
Each skill encodes a specific point of view on how something should be built — which libraries, which patterns, which tradeoffs. This means less decision fatigue and faster time-to-shipped.

**Skills compose.**
`project-scaffold` → `project-builder` → `project-workshop` forms a complete project lifecycle. `professional-frontend` pairs naturally with `eu-cookie-compliance`. Stack them.

**Skills are alive.**
As patterns evolve, skills get updated. The `.skill` format bundles reference docs alongside the trigger logic, so Claude always has current context — not a frozen snapshot.

---

## Repo structure

```
claude-skills/
├── 2fa-totp.skill               # TOTP 2FA implementation
├── doc-feature-extractor.skill  # Docs → feature map
├── eu-cookie-compliance.skill   # GDPR / ePrivacy consent
├── frontend-upgrade.skill       # Existing frontend improvement
├── messaging-agent.skill        # Telegram / Slack / Discord agent
├── monorepo-migration.skill     # Turborepo consolidation
├── professional-frontend.skill  # Design-system-first UI building
├── project-advisor.skill        # Repo audit & improvement report
├── project-builder.skill        # Scaffold → Review → Execute
├── project-scaffold.skill       # Idea → project scaffold
├── project-workshop.skill       # Full project lifecycle
└── x402-pos-terminal.skill      # x402 crypto POS terminal
```

---

<div align="center">

Built for [Claude Code](https://claude.ai/code) · Maintained by [@KingRaver](https://github.com/KingRaver)

</div>
