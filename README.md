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

Suppose a feature needs backend changes, a new interface and several rounds
of testing. Plan keeps the intended outcome, decisions, ordered tasks and
acceptance criteria in the repository. That gives the work a shared reference
beyond what any one chat remembers.

When I ask Workflow to run that Plan in Codex, a coordinator assigns bounded
pieces to worker chats. Code guides the implementation: understand the existing
code, change the responsible parts and verify the affected behavior. Where the
task includes an interface, UI adds guidance for structure, wording,
interaction and checks of the rendered result.

At the required review points, separate reviewers inspect the work. Findings
lead to corrections, while accepted results and remaining work are recorded
in the Plan. When a chat needs a successor, Workflow carries forward the
assignment and open issues. The next chat can continue from recorded progress
instead of reconstructing the project from a long conversation.

Setup manages the project's model and Workflow settings. If a question needs
another perspective, Ask can bring in independent advice from configured
Codex or Claude advisers. Handoff serves an explicitly requested transfer
outside Workflow too, collecting the current goal, decisions, unfinished work
and next action into a continuation prompt.

A small fix may only need Code, or Code and UI. Longer work benefits from Plan;
Workflow adds coordination when I want that Plan carried out across chats.
The Skills contribute where their roles are needed, without making every task
go through the full process.
