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

I develop a new Skill when project work exposes a gap I keep having to fill
myself. That might be explaining the same constraints again, recovering
decisions between chats or getting an agent to check its work. I define the
job the Skill should do and where its responsibility ends, then write
instructions and test cases around it.

Once a Skill is in use, I look at actual results and task histories to see
where it falls short. Did the agent miss an instruction, interpret it
differently than intended or spend time on work that did not help? Those
observations become test cases for improving the existing Skill.

I evaluate the responses, adjust the instructions and run the cases again.
I check whether the change solves the problem and whether it causes trouble
elsewhere. New experience from projects feeds into the next round of tests,
evaluation and adjustment.

That also means removing instructions that lead to repeated searches,
unnecessary checks or oversized output. I want the agent to have enough
direction to finish the task without making the process heavier than the
work requires.

Each Skill's description tells the agent which problems it helps solve and
when to use it. This is how the agent selects the relevant Skills as work
develops, including several when a task needs their different contributions.

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

For a feature that touches backend and interface, Plan records the goal,
decisions, tasks and acceptance criteria. When I ask Workflow to run it in
Codex, a coordinator assigns work to separate chats. Code guides implementation
and verification. UI adds interface structure, wording, interaction and
rendered checks.

Reviewers inspect the results, findings lead to corrections, and accepted
progress goes back into the Plan. Successor chats continue from that record
and the open issues, keeping longer work moving across context windows.

Setup controls model and Workflow settings. Ask brings in independent Codex
or Claude advice when needed. Handoff prepares a continuation prompt for
transfers outside Workflow.

A small fix may need only Code, or Code and UI. Plan and Workflow add
continuity and coordination when the work calls for them.
