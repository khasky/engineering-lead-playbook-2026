# Engineering Lead Playbook

Practical guide for senior and lead engineers on technical leadership, ownership, decision-making, mentoring, and execution.

> *If I were defining the role of a strong technical lead today, I would optimize for five things first: architectural judgment, delivery clarity, technical quality, multiplier behavior, and calm decision-making under ambiguity.*

---

## Table of Contents

- [Engineering Lead Playbook](#engineering-lead-playbook)
  - [Table of Contents](#table-of-contents)
  - [Why this exists](#why-this-exists)
  - [Companion playbooks](#companion-playbooks)
  - [The defaults I'd reach for first](#the-defaults-id-reach-for-first)
  - [What a lead engineer actually owns](#what-a-lead-engineer-actually-owns)
  - [Architecture without architecture theatre](#architecture-without-architecture-theatre)
    - [What I care about instead](#what-i-care-about-instead)
    - [A healthy architecture habit](#a-healthy-architecture-habit)
  - [Technical planning and roadmap shaping](#technical-planning-and-roadmap-shaping)
    - [What that usually requires](#what-that-usually-requires)
    - [What I would make visible](#what-i-would-make-visible)
  - [Code review as force multiplier](#code-review-as-force-multiplier)
    - [What I want code review to do](#what-i-want-code-review-to-do)
    - [What I would avoid in review](#what-i-would-avoid-in-review)
  - [Standards, RFCs, and decision records](#standards-rfcs-and-decision-records)
    - [Good candidates for written standards](#good-candidates-for-written-standards)
    - [Good candidates for RFCs or ADRs](#good-candidates-for-rfcs-or-adrs)
  - [Artifacts worth templating](#artifacts-worth-templating)
    - [ADR skeleton](#adr-skeleton)
    - [RFC outline](#rfc-outline)
    - [1:1 note structure](#11-note-structure)
  - [Mentoring and team leverage](#mentoring-and-team-leverage)
    - [Practical mentoring behavior](#practical-mentoring-behavior)
  - [Risk management and escalation](#risk-management-and-escalation)
    - [Risks I want surfaced early](#risks-i-want-surfaced-early)
  - [Leading during incidents](#leading-during-incidents)
    - [Roles first](#roles-first)
    - [While it burns](#while-it-burns)
    - [After it is out](#after-it-is-out)
  - [Cross-functional communication](#cross-functional-communication)
    - [What strong communication looks like](#what-strong-communication-looks-like)
  - [Measuring the system, not the people](#measuring-the-system-not-the-people)
    - [The four keys I'd start with](#the-four-keys-id-start-with)
    - [How I would read them](#how-i-would-read-them)
  - [What strong lead behavior looks like](#what-strong-lead-behavior-looks-like)
  - [Things I would avoid](#things-i-would-avoid)
  - [License](#license)

---

## Why this exists

Many engineers become senior because they can build difficult things.

That does **not** automatically teach them how to:

- create technical clarity for a team;
- shape architecture without overdesign;
- make delivery tradeoffs visible;
- mentor others effectively;
- prevent ambiguity from turning into drift.

This README is for that transition.

It treats technical leadership as a craft, not as a vague aura.

---

## Companion playbooks

These repositories form one playbook suite:

- [AI-Assisted Engineering Playbook](https://github.com/khasky/ai-assisted-engineering-playbook) — agent workflows, guardrails, and quality control for AI-heavy teams
- [API Design Playbook](https://github.com/khasky/api-design-playbook) — versioning, pagination, idempotency, error contracts, and webhooks
- [Auth & Identity Playbook](https://github.com/khasky/auth-identity-playbook) — sessions, tokens, OAuth, and identity boundaries across the stack
- [Backend Architecture Playbook](https://github.com/khasky/backend-architecture-playbook) — APIs, boundaries, OpenAPI, persistence, and errors
- [Best of JavaScript](https://github.com/khasky/best-of-javascript) — curated JS/TS tooling and stack defaults
- [Caching Playbook](https://github.com/khasky/caching-playbook) — HTTP, CDN, and application caches; consistency and invalidation
- [Code Review Playbook](https://github.com/khasky/code-review-playbook) — PR quality, ownership, and review culture
- [DevOps Delivery Playbook](https://github.com/khasky/devops-delivery-playbook) — CI/CD, environments, rollout safety, and observability
- **Engineering Lead Playbook** — standards, RFCs, and technical leadership habits
- [Frontend Architecture Playbook](https://github.com/khasky/frontend-architecture-playbook) — React structure, performance, and consuming API contracts
- [Git Collaboration Playbook](https://github.com/khasky/git-collaboration-playbook) — branching, stacked PRs, merge queues, and CI collaboration at scale
- [Marketing and SEO Playbook](https://github.com/khasky/marketing-and-seo-playbook) — growth, SEO, experimentation, and marketing surfaces
- [Messaging & Async Playbook](https://github.com/khasky/messaging-and-async-playbook) — queues, events, outbox, idempotent consumers, and retries
- [Monorepo Architecture Playbook](https://github.com/khasky/monorepo-architecture-playbook) — workspaces, package boundaries, and shared code at scale
- [Node.js Runtime & Performance Playbook](https://github.com/khasky/nodejs-runtime-performance-playbook) — event loop, streams, memory, and production Node performance
- [Observability Playbook](https://github.com/khasky/observability-playbook) — logs, traces, metrics, SLOs, and production visibility
- [React Cross-Platform Playbook](https://github.com/khasky/react-cross-platform-playbook) — shared React UI and logic across web and native with TypeScript
- [Software Design Playbook](https://github.com/khasky/software-design-playbook) — separation of concerns, composition, and module boundaries
- [State Management Playbook](https://github.com/khasky/state-management-playbook) — client state architecture, MobX, and choosing a state layer
- [Styling Architecture Playbook](https://github.com/khasky/styling-architecture-playbook) — type-safe styling, design tokens, and theming at scale
- [Testing Strategy Playbook](https://github.com/khasky/testing-strategy-playbook) — unit, integration, contract, E2E, and CI-friendly test layers

---

## The defaults I'd reach for first

If I were defining a strong lead-engineer operating model today, I would usually default to this:

- **Architecture decisions** captured with lightweight written rationale
- **Roadmaps** translated into explicit technical milestones and risks
- **Code reviews** used to raise the quality floor, not to display taste
- **Standards** written down where repeatable decisions exist
- **Mentoring** embedded into normal engineering flow
- **Escalation** early when scope, risk, or ownership is unclear
- **Cross-team communication** concise, factual, and decision-oriented
- **Delivery** optimized for steady progress over heroic crunches

That model scales better than charisma.

---

## What a lead engineer actually owns

The role is not "best coder in the room".

The role is closer to this:

- define and defend sane technical direction;
- reduce ambiguity for the team;
- make risk and tradeoffs visible early;
- help others make good decisions independently;
- connect architecture, delivery, and quality.

A lead engineer should make the team more predictable, not more dependent.

---

## Architecture without architecture theatre

Good technical leadership is not constant diagram production.

### What I care about instead

- clear system boundaries;
- fit-for-purpose design;
- visible tradeoffs;
- migration path, not just target state;
- explicit non-goals.

### A healthy architecture habit

Use lightweight RFCs or decision records when:

- multiple teams are affected;
- the choice is hard to reverse;
- there are real tradeoffs to document;
- future engineers will otherwise re-litigate the same decision.

Architecture becomes theatre when the document is more ambitious than the adoption plan.

---

## Technical planning and roadmap shaping

A lead engineer should be able to turn fuzzy goals into a credible technical path.

### What that usually requires

- decomposition into milestones;
- dependency mapping;
- identified risks and unknowns;
- spikes where uncertainty is real;
- sequencing that respects compatibility and rollout safety.

### What I would make visible

- what must happen first;
- what can run in parallel;
- what could block delivery;
- what technical debt is being created or paid down.

Leadership means making the invisible work legible.

---

## Code review as force multiplier

Code review is one of the highest-leverage leadership tools when used well.

### What I want code review to do

- protect correctness and maintainability;
- spread context;
- reinforce standards;
- improve design judgment;
- coach without grandstanding.

### What I would avoid in review

- performative nitpicking;
- endless style debates that tooling could solve;
- blocking on personal preference;
- using review to surprise people with major architectural objections too late.

Review should raise the system and the team at the same time.

---

## Standards, RFCs, and decision records

Great leads reduce recurring decision cost.

### Good candidates for written standards

- repository structure;
- API conventions;
- testing expectations;
- observability defaults;
- migration strategy;
- deployment safety checks.

### Good candidates for RFCs or ADRs

- service decomposition;
- new data ownership boundaries;
- platform choices;
- large migrations;
- major dependency adoption.

Write things down where repetition or reversibility justifies it.

---

## Artifacts worth templating

Most decisions go unrecorded because the write-up feels expensive.

A template's job is to make writing cheaper than re-arguing.

### ADR skeleton

One page maximum. If it needs more, it is an RFC.

```text
# ADR-014: <decision title>

Status: proposed | accepted | superseded by ADR-021
Context: what forced a decision now
Decision: what we chose, in one or two sentences
Consequences: what gets easier, what gets harder, what we gave up
```

### RFC outline

```text
# RFC: <proposal title>

Problem: what hurts and who feels it
Constraints: what any solution must respect
Options considered: two or three, with real tradeoffs
Recommendation: which option and why
Rollout: migration path, sequencing, rollback
Open questions: what review should resolve
```

### 1:1 note structure

```text
## <date> — <name>

Their agenda: always first
Growth thread: the ongoing skill or scope conversation
Actions: who does what, by when
```

If filling the template takes longer than the decision took to make, shrink the template.

---

## Mentoring and team leverage

A strong lead does not only solve problems personally.

They increase the number of people who can solve them well.

### Practical mentoring behavior

- explain tradeoffs, not just answers;
- delegate meaningful ownership;
- review design, not only implementation;
- give early feedback before a week of work drifts;
- encourage documentation and system thinking.

Teaching is not separate from delivery.  
It is part of scaling delivery.

---

## Risk management and escalation

A lot of technical leadership is really risk management with better vocabulary.

### Risks I want surfaced early

- hidden coupling;
- migration complexity;
- test gaps;
- ambiguous ownership;
- delivery dependencies on one person;
- release or rollback weakness.

Escalation is not failure.  
Late surprise is failure.

---

## Leading during incidents

The lead's job in an incident is calm coordination, not heroic typing.

### Roles first

- one incident commander who coordinates and communicates;
- hands-on responders who investigate and fix;
- never the same person doing both for long.

### While it burns

- a steady communication cadence to stakeholders: what we know, what we are doing, when the next update comes;
- rehearsed runbooks over improvisation — mid-incident is the worst time to design a procedure;
- decisions logged as they happen, so the postmortem is not archaeology.

### After it is out

- blameless postmortems that end in systemic fixes: trace to where the failure originated, not where it paged — the same root-cause discipline the [Observability Playbook](https://github.com/khasky/observability-playbook) applies to production signals;
- follow-up work protected from roadmap pressure: an action item nobody schedules is a repeat incident with a future date.

The measure of incident leadership is the second incident that never happens.

---

## Cross-functional communication

Senior and lead engineers often underinvest here.

### What strong communication looks like

- concise status with facts and implications;
- clear asks from product, design, or leadership;
- transparent tradeoffs when timelines change;
- technical framing translated into business consequence.

You do not need to speak like a PM.  
You do need to make technical reality understandable.

---

## Measuring the system, not the people

Delivery metrics describe the system the team works inside.

They never describe individuals.

### The four keys I'd start with

- deployment frequency;
- lead time for changes;
- change failure rate;
- time to restore service.

These are DORA's four keys, and they answer one question: how safely and quickly can this team's system turn a change into production value?

### How I would read them

- trends over absolutes: direction matters more than any single number;
- pair them with SLO health so speed never hides reliability debt — covered in depth in the [Observability Playbook](https://github.com/khasky/observability-playbook);
- never as individual performance metrics: the moment a number judges a person, people optimize the number instead of the system.

Beware metric theatre.  
A dashboard nobody acts on is decoration; if a metric never changes a decision, delete it.

---

## What strong lead behavior looks like

A lead engineer is usually doing well when:

- the team knows why a decision was made;
- architecture docs are short but useful;
- risks appear earlier in the project, not at the deadline;
- the team can move without waiting for one person;
- quality is improving through standards, not heroics.

That is what "senior presence" often looks like in practice.

---

## Things I would avoid

- trying to personally own every important change;
- architecture documents with no rollout plan;
- vague standards nobody can apply in code review;
- using seniority as taste authority instead of reasoning authority;
- delaying escalation to "protect" the team from visibility;
- mentoring only after things go wrong.

---

## License

MIT is a sensible default for a playbook repository like this, but choose the license that fits your sharing goals.
