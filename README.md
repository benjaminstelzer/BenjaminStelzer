# Benjamin Stelzer

I build practical Agent Skills and developer tools for Codex, Claude Code, and
AI-assisted software work.

## Why this work?

I use AI agents for real projects, and I keep running into the same problems.
An agent adds structure before understanding the existing code, rewrites a
sentence and changes its meaning, or reports a result it has not checked.

My Skills put instructions around those failures. They should help the agent
finish the actual task without making every small change a process of its own.

## How I work

I start with the result I need and the project that already exists. Its code,
terminology and decisions matter more than a new abstraction or a cleaner
description of something that is still wrong.

I use the Skills in my own work, then read complete task histories alongside
the results. That shows where instructions help, where they fail and where
repeated searches, unnecessary checks or oversized output waste context. I
revise the instructions around those observations and test the affected cases.

I also use SkillOpt and other optimization runs. They help explore changes,
including shorter instructions, but I do not keep a proposal just because an
optimizer produced it. Each Skill has a specific job and can work on its own.
I combine them when the task needs more than one of those jobs.

## Scoville Family

[Scoville Suite](https://github.com/benjaminstelzer/scoville-suite) brings the
Skills together. Its Codex-only Workflow coordinates plan-driven execution
and is available with the suite, not as a separate repository. Each specialist
Skill retains its own scope and host requirements.

- [Scoville Brainstorm](https://github.com/benjaminstelzer/scoville-brainstorm)
  explores materially different mechanisms before selection.
- [Scoville Research](https://github.com/benjaminstelzer/scoville-research)
  turns web, GitHub, and scholarly evidence into a decision-ready,
  claim-traceable result.
- [Scoville Code](https://github.com/benjaminstelzer/scoville-code-anti-ai-slop)
  owns engineering scope, implementation, risk, and validation.
- [Scoville Design](https://github.com/benjaminstelzer/scoville-design-anti-ai-slop)
  owns visual definition, art direction, design systems, critique and repair.
- [Scoville UI](https://github.com/benjaminstelzer/scoville-ui-anti-ai-slop)
  owns framework-aligned implementation, interface mechanics, accessibility,
  and rendered evidence, with a standalone design fallback.
- [Scoville WordPress UI Backend](https://github.com/benjaminstelzer/scoville-wordpress-ui-backend-anti-ai-slop)
  owns plugin-owned WordPress admin interfaces, platform components, spacing,
  accessibility and internationalization.
- [Scoville Scribe](https://github.com/benjaminstelzer/scoville-scribe-anti-ai-slop)
  owns wording, terminology, factual meaning, and source fidelity.
- [Scoville Plan](https://github.com/benjaminstelzer/scoville-plan) owns durable
  Plans, Work Items, Decisions, and lifecycle state.
- [Scoville Handoff](https://github.com/benjaminstelzer/scoville-handoff)
  transfers active work to another agent or session.

## Ask Family

[Ask Suite for Codex](https://github.com/benjaminstelzer/ask-suite-for-codex)
groups the independent second-opinion Skills for Codex.

- [Ask Claude for Codex](https://github.com/benjaminstelzer/ask-claude-for-codex)
  gives Codex a read-only second opinion from Claude Code with selectable model,
  reasoning effort, budget, and persistent conversations.
- [Ask Claude and SOL for Codex](https://github.com/benjaminstelzer/ask-claude-and-sol-for-codex)
  runs Claude Code and a separate SOL session in parallel, returns both
  read-only opinions together, and preserves both conversations for follow-up
  questions.
- [Ask Claude and Astra for Codex](https://github.com/benjaminstelzer/ask-claude-and-astra-for-codex)
  pairs Claude Code with a fresh Astra project task and keeps both conversations
  available for follow-up questions.
- [Ask Astra for Review for Codex](https://github.com/benjaminstelzer/ask-astra-for-review-for-codex)
  sends questions and review requests to a fresh Astra project task, returns its
  answer directly, and keeps the task open for follow-up questions. The adviser
  asks before archiving it.
- [Ask SOL for Review for Codex](https://github.com/benjaminstelzer/ask-sol-for-review-for-codex)
  sends a read-only review request to a fresh SOL project task.

## How it fits together

Start with the part that solves your problem. Code covers engineering work,
Scribe covers wording and meaning, and Plan keeps longer work recoverable.
The other repositories explain their own scope, setup and development.

If you are building Skills yourself, the instructions and development accounts
show the choices behind mine. They are projects I keep revising through use.
