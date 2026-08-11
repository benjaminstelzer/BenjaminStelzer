# Benjamin Stelzer

I build practical Agent Skills and developer tools for Codex, Claude Code, and
AI-assisted software work.

The projects share one concern: an AI agent can produce a great deal of motion
without necessarily producing the result that was asked for. My tools keep the
result, the boundaries, and the evidence visible while the machinery does its
machinery.

## Why this work?

AI agents are useful precisely because they can move quickly across code,
research, planning, and writing. The catch is not that they do too little. It is
that they can do a convincing amount of the wrong thing: another abstraction,
another plan, another polished paragraph, and suddenly the process has eaten
the task.

I build small, explicit contracts around those failure points. Not to make an
agent timid, and not to turn every rename into a governance summit. The aim is
to let it move quickly without losing ownership, meaning, authority, or the
difference between evidence and optimism.

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

## Agent Skills

- [Ask Claude for Codex](https://github.com/benjaminstelzer/ask-claude-for-codex)
  gives Codex a read-only second opinion from Claude Code with selectable model,
  reasoning effort, budget, and persistent conversations.
- [Scoville Brainstorm](https://github.com/benjaminstelzer/scoville-brainstorm)
  explores materially different mechanisms before selection.
- [Scoville Code](https://github.com/benjaminstelzer/scoville-code-anti-ai-slop)
  owns engineering scope, implementation, risk, and validation.
- [Scoville UI](https://github.com/benjaminstelzer/scoville-ui-anti-ai-slop)
  owns interface hierarchy, framework fit, accessibility, and rendered
  evidence.
- [Scoville Scribe](https://github.com/benjaminstelzer/scoville-scribe-anti-ai-slop)
  owns wording, terminology, factual meaning, and source fidelity.
- [Scoville Plan](https://github.com/benjaminstelzer/scoville-plan) owns durable
  Plans, Work Items, Decisions, and lifecycle state.
- [Scoville Handoff](https://github.com/benjaminstelzer/scoville-handoff)
  transfers active work to another agent or session.

## Codex prompt

- [Codex, Fable-calibrated style](https://github.com/benjaminstelzer/codex-fable-like-system-prompt-for-gpt-5.6-sol)
  keeps Codex's operating machinery and changes the collaboration layer:
  direct conclusions, explicit reasoning, honest limits, and less conversational
  padding.

## How it fits together

The system prompt governs general collaboration. A selected Agent Skill adds a
narrower contract for the task at hand. Scoville Scribe owns meaning and
fidelity; Scoville Code owns engineering, and neither gets to borrow authority
from a nice sentence.

Project-specific scope, installation, evidence, sources, and licensing stay in
the repositories that define them. Install only the part that solves the actual
problem. The collection is a toolbox, not a loyalty program.

## Status

These repositories are independent projects with their own release history and
validation where applicable. Current behavior, compatibility, and measured
results stay with each project rather than in a profile snapshot that ages
quietly and then acts surprised.
