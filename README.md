# Benjamin Stelzer

I build Agent Skills and developer tools for the software projects I work on
with Codex and Claude Code.

## Why this work?

I use AI agents for real projects, and I keep running into the same problems.
An agent adds structure before understanding the existing code, loses earlier
decisions as work continues, or reports a result it has not checked.

My Skills grew out of those failures. They help agents work within an existing
codebase, build usable interfaces, check results and carry the goal and progress
across conversations. The aim is to finish the actual task with fewer repeated
explanations, unnecessary changes and unsupported claims.

Scoville Workflow extends this to longer autonomous work. In my projects,
it lets agents work through planned tasks over several days with very little
intervention from me. Workers implement and test changes, independent reviewers
check the results, and findings feed back into corrections. This loop helps
catch mistakes before later work builds on them and reduces the risk of
autonomous changes drifting away from the plan.

The suite with Workflow is currently available only for Codex, my daily driver.
A Claude version with Workflow is also planned. The general Scoville Suite
already supports Claude Code and other harnesses without Workflow.

## How I work

A new Skill starts with a recurring problem in my own projects. Before writing
instructions, I work out what it needs to solve and whether that belongs in
an existing Skill. A separate Skill needs a clear responsibility, with test
cases that make its boundaries visible.

To improve existing Skills, I analyze extensive test runs alongside complete
project conversations. Over the past months, that has helped me understand
where agents go wrong and which instructions need to change. A plausible
answer can hide a missed requirement. A useful safeguard can turn into layers of checks
that cost more than the problem warrants. The full sequence of implementation,
review and correction shows patterns a single response can miss.

Those findings feed into test cases, revised instructions and another round
of evaluation. I compare the new results with earlier runs, checking both the
original failure and effects elsewhere. Repeated searches, unnecessary checks
and oversized output matter too: they consume time and context that the agent
needs for the actual work.

I deliberately test with smaller models than the ones I use day to day.
The instructions need to be clear enough for those models to follow, rather
than relying on a stronger model to fill in missing context or resolve
ambiguities. Failures in those runs help me find where the wording or sequence
still needs work.

Skill selection gets its own targeted tests. These cover requests near the
boundary between Skills, tasks that need several Skills and cases where a
Skill should stay out. I use the results to sharpen descriptions and separate
responsibilities based on which Skills the agent actually selects and how
it applies them.

## Scoville Family

Choose the complete [Scoville Suite](https://github.com/benjaminstelzer/scoville-suite)
for general Agent Skills hosts, including Claude Code, or the
[Scoville Suite for Codex](https://github.com/benjaminstelzer/scoville-suite-for-codex)
for Codex. Both include Code, Plan, UI and Handoff. The Codex suite also includes
Workflow, Ask and Setup. Workflow and Setup are available only in that suite.

- [Scoville Workflow for Codex](https://github.com/benjaminstelzer/scoville-suite-for-codex/tree/main/members/scoville-workflow-for-codex)
  runs a repository Plan through separate worker, reviewer and successor chats,
  keeping long tasks directed beyond one context window.
- [Scoville Code](https://github.com/benjaminstelzer/scoville-code)
  guides implementation, diagnosis and review, with checks proportionate to
  the consequences of a mistake.
- [Scoville Plan](https://github.com/benjaminstelzer/scoville-plan)
  records goals, tasks, decisions and progress so another session can resume
  the work.
- [Scoville UI](https://github.com/benjaminstelzer/scoville-ui)
  implements and checks interfaces through their framework and design system,
  including plugin-owned WordPress admin pages.
- [Scoville Handoff](https://github.com/benjaminstelzer/scoville-handoff)
  transfers active work to another agent or session.
- [Scoville Ask for Codex](https://github.com/benjaminstelzer/scoville-ask-for-codex)
  gets independent read-only advice from configured Codex or Claude advisers.

Individual repositories provide standalone packages. Suite installations use
the complete package set from the chosen suite.

## How it fits together

For a feature that touches backend and interface, Plan records the goal,
decisions, tasks and acceptance criteria. When I ask Workflow to run it in
Codex, a coordinator assigns work to separate chats. Code guides implementation
and verification. UI guides structure, wording and interaction, with checks
of the rendered interface.

Reviewers inspect the results, findings lead to corrections, and accepted
progress goes back into the Plan. Successor chats continue from that record
and the open issues, keeping longer work moving across context windows.

Setup controls model and Workflow settings. Ask brings in independent Codex
or Claude advice when needed. Handoff prepares a continuation prompt for
transfers outside Workflow.

A small fix may need only Code, or Code and UI. Plan and Workflow add
continuity and coordination when the work calls for them.
