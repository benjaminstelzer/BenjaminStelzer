# Benjamin Stelzer

I build practical Agent Skills and developer tools for Codex, Claude Code, and
AI-assisted software work.

## Why this work?

I use AI agents for real projects, and I keep running into the same problems.
An agent adds structure before understanding the existing code, loses earlier
decisions as work continues, or reports a result it has not checked.

My Skills grew out of those failures. They help agents work within an existing
codebase, build usable interfaces, check results and carry the goal and progress
across conversations. The aim is to finish the actual task with fewer repeated
explanations, unnecessary changes and unsupported claims.

Each Skill addresses a specific gap I encountered in project work, keeping
the effort proportionate to the task.

## How I work

I start with the result I need and the project that already exists. Its code,
terminology and decisions matter more than a new abstraction or a cleaner
description of something that is still wrong.

I use the Skills in real projects and have complete task histories analyzed
alongside the results. Those analyses help identify where instructions fail,
where they leave too much room for interpretation and where repeated searches,
unnecessary checks or oversized output waste context.

I combine targeted simulation runs with several optimization workflows,
including SkillOpt. This is an iterative process over months: problems from
real projects feed into corrections, the affected cases are tested, and the
Skills are refined again as new problems emerge. An optimization proposal is
something to test, not a reason to keep the change.

Each Skill has a specific job and works independently. I combine them when
the task needs more than one of those jobs.

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
  owns engineering scope, implementation, risk and validation.
- [Scoville Plan](https://github.com/benjaminstelzer/scoville-plan)
  keeps Plans, Work Items and Decisions recoverable across sessions.
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

Start with the part that solves your problem. Code covers engineering work,
UI covers interfaces, Plan keeps longer work recoverable, and Workflow runs
a Plan across Codex chats.
The other repositories explain their own scope, setup and development.

If you are building Skills yourself, the instructions and development accounts
show the choices behind mine. They are projects I keep revising through use.
