# Benjamin Stelzer

I build practical Agent Skills and developer tools for Codex, Claude Code, and
AI-assisted software work.

## Why this work?

AI agents can produce a convincing amount of the wrong thing: another
abstraction, another plan, another polished paragraph, and suddenly the process
has eaten the task.

I build small, explicit contracts around those failure points so agents can
move quickly without losing ownership, meaning, authority, or evidence.

## How I work

- **The result comes first.** Process earns its place by making the requested
  outcome safer, clearer, or easier to verify.
- **Facts survive presentation.** Better prose, cleaner UI, and tighter
  summaries do not get permission to improve the underlying truth into
  something else.
- **Boundaries stay visible.** A read-only review does not become an edit, a
  suggestion does not become authority, and a passing check proves only what it
  exercised.
- **Tools stay composable.** Each Skill owns one concern and can work alone.
  Combining everything by default would merely produce a very organized kind
  of confusion.

## Scoville family

- [Scoville Brainstorm](https://github.com/benjaminstelzer/scoville-brainstorm)
  explores materially different mechanisms before selection.
- [Scoville Research](https://github.com/benjaminstelzer/scoville-research)
  turns web, GitHub, and scholarly evidence into a decision-ready,
  claim-traceable result.
- [Scoville Code](https://github.com/benjaminstelzer/scoville-code-anti-ai-slop)
  owns engineering scope, implementation, risk, and validation.
- [Scoville Design](https://github.com/benjaminstelzer/scoville-design-anti-ai-slop)
  owns visual definition, art direction, design systems, critique, and repair.
- [Scoville UI](https://github.com/benjaminstelzer/scoville-ui-anti-ai-slop)
  owns framework-aligned implementation, interface mechanics, accessibility,
  and rendered evidence, with a standalone design fallback.
- [Scoville Scribe](https://github.com/benjaminstelzer/scoville-scribe-anti-ai-slop)
  owns wording, terminology, factual meaning, and source fidelity.
- [Scoville Plan](https://github.com/benjaminstelzer/scoville-plan) owns durable
  Plans, Work Items, Decisions, and lifecycle state.
- [Scoville Handoff](https://github.com/benjaminstelzer/scoville-handoff)
  transfers active work to another agent or session.

## WordPress Skills

- [WordPress Backend UI](https://github.com/benjaminstelzer/wordpress-backend-ui-skill)
  defines the UI contract for plugin-owned WordPress 7 backends: surface
  ownership, vertical flow, responsive behavior, accessibility, i18n, and
  WordPress defaults before custom CSS.

## Codex Skills

- [Ask Claude for Codex](https://github.com/benjaminstelzer/ask-claude-for-codex)
  gives Codex a read-only second opinion from Claude Code with selectable model,
  reasoning effort, budget, and persistent conversations.
- [Ask Claude and SOL for Codex](https://github.com/benjaminstelzer/ask-claude-and-sol-for-codex)
  runs Claude Code and a separate SOL session in parallel, returns both
  read-only opinions together, and preserves both conversations for follow-up
  questions.

- [Ask Claude and Astra for Codex](https://github.com/benjaminstelzer/ask-claude-and-astra-for-codex)
  pairs Claude Code with a fresh Astra subagent, using Astra with xhigh effort
  by default and keeping both conversations available for follow-up questions.

## How it fits together

A selected Agent Skill adds a contract for the task at hand. Scoville Scribe
owns meaning and fidelity. Scoville Code owns engineering. Neither gets to borrow authority
from a nice sentence.

Project-specific scope, installation, evidence, sources, and licensing stay in
the repositories that define them. Install only the part that solves the actual
problem. The collection is a toolbox, not a loyalty program.

## Status

These repositories are independent projects with their own release history and
validation where applicable. Current behavior, compatibility, and measured
results stay with each project rather than in a profile snapshot that ages
quietly and then acts surprised.
