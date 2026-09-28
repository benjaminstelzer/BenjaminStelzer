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

Scoville Workflow extends this to longer autonomous work. In my projects,
it lets agents work through planned tasks over several days with very little
intervention from me. Workers implement and test changes, independent reviewers
check the results, and findings feed back into corrections. This loop helps
catch mistakes before later work builds on them and reduces the risk of
autonomous changes drifting away from the plan.

The suite with Workflow is currently available only for Codex, my daily driver.
A Claude version with Workflow is also planned. The general Scoville Suite
already supports Claude Code and other harnesses without Workflow.

Each Skill addresses a specific gap I encountered in project work, keeping
the effort proportionate to the task.

## How I work

Most improvements start with something that went wrong in a real project.
I look at the result and the task history to understand what led to it.
Did the agent miss an instruction, interpret it differently than intended,
or spend too much time on work that did not help?

I turn those observations into test cases, evaluate the responses and adjust
the instructions. Then I run the cases again to see whether the change helps
and whether it causes problems elsewhere. New project experience adds new
cases, so the Skills keep evolving through that cycle of testing, evaluation
and adjustment.

I also look for repeated searches, unnecessary checks and oversized output
that consume context without improving the result. The aim is to give agents
enough direction to solve the problem while keeping the work proportionate.

Each Skill has a specific job. Its description helps the agent recognize when
that job is needed and select the relevant Skills as work develops. Several
can contribute when a task spans their roles.

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
