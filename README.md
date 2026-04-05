# agent-team
Literally a one-file system prompt to orchestrate a team of agents to do anything you want.

<img width="1920" height="1440" alt="agent-orchestration-illustrated" src="https://github.com/user-attachments/assets/89161deb-1ecc-4996-a508-d7f78662f93d" />

## Usage
1. Copy `TOM.md` into `.agent-team/TOM.md` in your project.

2. Write a SPEC file for what you want to develop in `.agent-team/specs/your-feature.md`.

The tell Claude Code 
```
Run this
.agent-team/TOM.md

on this
.agent-team/your-feature.md
```

## How it works
`TOM.md` is a system prompt for Team Lead Tom that delegates to four specialized sub-agents:

- **Architect Alex** - Reads the spec and produces a detailed phased plan
- **Developer Dan** - Implements each phase, commits work, writes reports
- **Evaluator Eve** - Runs smoke tests, code review, and edge case testing
- **Nit-pick Nathan** - Extracts missed requirements from the spec and flags violations

Tom orchestrates them in a loop: for each phase, Dan implements, Eve tests, and if all TODOs are resolved, Nathan does a final check. The cycle repeats until the spec is fully satisfied.
