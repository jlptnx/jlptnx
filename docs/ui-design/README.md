# UI Design Documentation — JLPT Pass Pods

Welcome to the UI design documentation for JLPT Pass Pods.

---

## Quick Links

| Document | Description |
|----------|-------------|
| [ICP Architecture](./architecture/ICP-ARCHITECTURE.md) | Information-Container-Presentation pattern overview |
| [User Journeys](./workflows/USER-JOURNEYS.md) | User workflows and journey maps |
| [Screen Specifications](./screens/SCREEN-SPECIFICATIONS.md) | Detailed screen wireframes and ICP breakdown |
| [Design System](./components/DESIGN-SYSTEM.md) | Colors, typography, and component library |

---

## Project Overview

**JLPT Pass Pods** is a language-learning web app that helps learners pass the JLPT through small-group accountability pods.

### Core Value Proposition

> Transform JLPT preparation from a solo, fragile habit into a shared, resilient system designed to get learners across the finish line.

### Key Features

1. **Study Pods** — Small groups (3-8 people) aligned to JLPT level and exam date
2. **Daily Check-ins** — Proof-based study logs with streak tracking
3. **Weekly Reviews** — Reflect on progress and set goals
4. **AI Coaching** — Lightweight insights to identify blockers and suggest adjustments

---

## Architecture Pattern

We use **ICP (Information-Container-Presentation)** to separate concerns:

```
┌─────────────────────────────────────────────────────────┐
│                    PRESENTATION                         │
│         (Visual components, layouts, styling)           │
├─────────────────────────────────────────────────────────┤
│                     CONTAINER                           │
│      (State management, business logic, handlers)       │
├─────────────────────────────────────────────────────────┤
│                    INFORMATION                          │
│        (Data models, API contracts, data flow)          │
└─────────────────────────────────────────────────────────┘
```

See [ICP Architecture](./architecture/ICP-ARCHITECTURE.md) for details.

---

## Screen Priority

| Priority | Screens |
|----------|---------|
| **P0** | Dashboard, Daily Check-In, Onboarding, Auth |
| **P1** | Pod Detail, Weekly Review, Pod Browser, Settings |
| **P2** | Create Pod, AI Coach, Landing Page |

---

## Design Principles

1. **Clarity Over Cleverness** — Interface should be invisible
2. **Momentum, Not Guilt** — Celebrate progress, encourage recovery
3. **Compact Information Density** — Scannable in seconds
4. **Japanese-Friendly** — Support mixed JP/EN text beautifully

---

## Directory Structure

```
docs/ui-design/
├── README.md                              # This file
├── architecture/
│   └── ICP-ARCHITECTURE.md                # Pattern documentation
├── workflows/
│   └── USER-JOURNEYS.md                   # User flows and journeys
├── screens/
│   └── SCREEN-SPECIFICATIONS.md           # Screen wireframes
└── components/
    └── DESIGN-SYSTEM.md                   # Design tokens and components
```

---

## Next Steps

- [ ] Create high-fidelity mockups in Figma
- [ ] Build component library in code (packages/ui-components)
- [ ] Implement P0 screens in web app
- [ ] User testing with JLPT learners
