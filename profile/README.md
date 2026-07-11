# frontier-infra

**Open-source primitives for AI-first applications.**

We build the missing infrastructure layers between web applications and AI agents. Every project here is agentic-first — designed for a world where AI is a first-class consumer of software, not an afterthought bolted on top.

---

## Projects

### [The Machine](https://github.com/frontier-infra/the-machine)

The harness, not the model. The prompt is the job ticket; The Machine is the operating system — durable state, a dumb deterministic driver, fresh workers, and verification against reality instead of self-report.

Everything else in the stack is a deployment of this pattern, or verifies against it. machine-driver and Conductor are its two reference drivers; Maintainer Gate Blueprint and Agent Control Plane build governance and proof on top of it.

```bash
python -m kit score <path-to-deployment-repo>   # dated, evidence-cited L0–L5 packet
python -m kit matrix                            # render the test matrix
```

**Conformance is run, not asserted.** A deployment earns a level — L0 Look-Alike through L5 Trusted Autonomy — via the kit; it doesn't claim one.

[Read the spec](https://github.com/frontier-infra/the-machine/blob/main/THE-MACHINE.md)

### [AVL — Agent View Layer](https://github.com/frontier-infra/avl)

Producer-side rendering for AI agents. Like i18n, but the target locale is "agent."

Web apps already know their intent, their data, their permissions, and their affordances — then they throw it all away to render pixels. AVL flips this: every page ships a parallel agent-native view alongside the human HTML. Same data, same auth, different rendering target.

```
/dashboard        → human view (HTML)
/dashboard.agent  → agent view (text/agent-view)
```

```bash
npm install @frontier-infra/avl
```

**MCP is the hands. AVL is the eyes.**

[Read the thesis](https://github.com/frontier-infra/avl/blob/main/specs/avl-thesis.md) ·
[Read the spec](https://github.com/frontier-infra/avl/blob/main/specs/avl-agent-view-layer.md) ·
[Get started](https://github.com/frontier-infra/avl#getting-started)

### The rest of the stack

The Machine is the govern tier everything else plugs into. The rest of Frontier Infra covers declare, behave, enforce, operate, and prove — a full loop for reliable, long-running agent work:

- **[AVL — Agent View Layer](https://github.com/frontier-infra/avl)** (declare) — a parallel agent-native view shipped alongside the human HTML for every page.
- **[ADL — Agent Discipline Layer](https://github.com/frontier-infra/adl)** (behave) — layered guardrails plus a goal contract that Warden verifies against reality before a Claude Code session can end.
- **[Proctor](https://github.com/frontier-infra/proctor)** (enforce) — the machine-level engine behind ADL: makes an agent's "done" a verified fact instead of a claim.
- **[machine-driver](https://github.com/frontier-infra/machine-driver)** and **[Conductor](https://github.com/frontier-infra/conductor)** (operate) — the two reference drivers for The Machine: one drives code work, the other drives multi-agent ops triage.
- **[Maintainer Gate Blueprint](https://github.com/frontier-infra/Maintainer-Gate-Blueprint)** (govern) — reusable ops model for repos where AI agents work in parallel: patrol loops, PR quality gates, machine-checkable handoffs.
- **[Agent Control Plane / AAR](https://github.com/frontier-infra/agentcontrolplane)** (prove) — Agent Attestation Record: portable, signed, ground-truthed proof of what an agent actually did.
- **[Roundtable](https://github.com/frontier-infra/roundtable)** (decide) — convene a council of frontier models — Grok, Codex/OpenAI, GLM, MiniMax, Claude, Gemini — from the CLI or any MCP harness.

See it all running together in **[stack-demo](https://github.com/frontier-infra/stack-demo)** — a live board whose every claim links a cryptographic receipt you can verify yourself.

---

## Philosophy

- **The agent is not a scraper.** Applications should render for AI agents the same way they render for non-English speakers — with a parallel, first-class view owned by the producer, not reverse-engineered by the consumer.
- **Same session, different render.** AI agents inherit existing human sessions. No new auth surface, no new API keys, no second permission model to maintain.
- **Ship small, compose well.** Every package here is zero-dependency where possible, framework-agnostic at the core, with thin adapters for specific runtimes.
- **Start cheap, get value immediately.** Conformance ramps (L0 → L3) let teams ship value in hours and expand incrementally.
- **Witness, don't trust self-report.** Evidence comes from tool output and signed, checkable records — never from an agent's own account of itself.

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
- **Try the discipline layer** — install ADL and Proctor in a Claude Code repo and see what they catch
- **Join the conversation** in [Discussions](https://github.com/frontier-infra/avl/discussions)

---

*Infrastructure for the agent-native web.*
