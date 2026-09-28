# Benjamin Stelzer

I build Agent Skills for reliable, verifiable software changes, from a focused
fix to planned work across several days. Scoville Code provides the engineering
foundation, with the rest of the suite supporting interfaces, planning,
review and coordination.

## Why this work?

I use AI agents for real projects, and I keep running into the same problems.
An agent adds structure before understanding the existing code, loses earlier
decisions as work continues, or reports a result it has not checked.

I built the suite around Scoville Code because reliable changes are the
starting point. Code guides the agent to understand the existing code, find
the cause and make a focused change. The result needs evidence of what works
and a clear account of what remains unchecked.

Scoville Workflow carries that approach into longer tasks. In my projects,
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
cases that make its boundaries visible. UI, for example, adds the interface
decisions and rendered checks that belong alongside Code's engineering rules.

To improve existing Skills, I analyze extensive test runs alongside complete
project conversations. Over the past months, that has helped me understand
where agents go wrong and which instructions need to change. A plausible
answer can hide a missed requirement. A useful safeguard can turn into layers
of checks that cost more than the problem warrants. The full sequence of implementation,
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
  provides the shared engineering rules for implementation, diagnosis and
  review, with evidence proportionate to the consequences of a mistake.
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
Codex, a coordinator assigns work to separate chats. Workers apply Code's
engineering rules and UI's interface guidance to the assigned changes.
The Plan defines what must be achieved, and those Skills guide how to get
there and check the result.

Reviewers inspect the results, findings lead to corrections, and accepted
progress goes back into the Plan. Successor chats continue from that record
and the open issues, keeping longer work moving across context windows.

Setup controls model and Workflow settings. Ask brings in independent Codex
or Claude advice when needed. Handoff prepares a continuation prompt for
transfers outside Workflow.

For a small fix, Code may be enough. Larger work adds the planning, interface
guidance and coordination it needs, while keeping the same expectation:
focused changes with results that can be checked.
