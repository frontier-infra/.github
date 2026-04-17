# frontier-infra

**Open-source primitives for AI-first applications.**

We build the missing infrastructure layers between web applications and AI agents. Every project here is agentic-first — designed for a world where AI is a first-class consumer of software, not an afterthought bolted on top.

---

## Projects

### [AVL — Agent View Layer](https://github.com/frontier-infra/avl)

Producer-side rendering for AI agents. Like i18n, but the target locale is "agent."

Web apps already know their intent, their data, their permissions, and their affordances — then they throw it all away to render pixels. AVL flips this: every page ships a parallel agent-native view alongside the human HTML. Same data, same auth, different rendering target.

```
/dashboard       → human view (HTML)
/dashboard.agent → agent view (text/agent-view)
```

```bash
npm install @frontier-infra/avl
```

**MCP is the hands. AVL is the eyes.**

[Read the thesis](https://github.com/frontier-infra/avl/blob/main/specs/avl-thesis.md) ·
[Read the spec](https://github.com/frontier-infra/avl/blob/main/specs/avl-agent-view-layer.md) ·
[Get started](https://github.com/frontier-infra/avl#getting-started)

---

## Philosophy

- **The agent is not a scraper.** Applications should render for AI agents the same way they render for non-English speakers — with a parallel, first-class view owned by the producer, not reverse-engineered by the consumer.
- **Same session, different render.** AI agents inherit existing human sessions. No new auth surface, no new API keys, no second permission model to maintain.
- **Ship small, compose well.** Every package here is zero-dependency where possible, framework-agnostic at the core, with thin adapters for specific runtimes.
- **Start cheap, get value immediately.** Conformance ramps (L0 → L3) let teams ship value in hours and expand incrementally.

---

## From the Lab

frontier-infra is the open-source arm of [Jason Brashear](https://jasonbrashear.com) — 30+ years in infrastructure (Cisco CCIE, Red Hat CE, Dell, Apple, AMD), now building at the intersection of AI agents and web infrastructure.

Writing about the agentic-first future at **[Frontier Operations](https://jasonbrashear.substack.com/)** on Substack.

### Related Projects

- **[Argent OS](https://github.com/webdevtodayjason)** — AI agent operating system. AVL is the substrate Argent OS uses to navigate any host application.
- **[AInode.dev](https://ainode.dev)** — AI-native development platform.

---

## Get Involved

We're looking for early adopters, framework implementations, and real-world feedback.

- **Use AVL** in your Next.js app and tell us what breaks
- **Build an adapter** for SvelteKit, Remix, Nuxt, or Rails
- **Write an agent** that consumes `.agent` URLs natively
- **Join the conversation** in [Discussions](https://github.com/frontier-infra/avl/discussions)

---

*Infrastructure for the agent-native web.*
