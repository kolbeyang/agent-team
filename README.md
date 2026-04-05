# agent-team

A prompt-based orchestration framework for managing a team of AI coding agents. Give it a spec and it coordinates a full development cycle: planning, implementation, QA testing, and nitpick review.

## How it works

`TOM.md` is a system prompt for a "Team Lead" agent that delegates to four specialized sub-agents:

- **Architect Alex** - Reads the spec and produces a detailed phased plan
- **Developer Dan** - Implements each phase, commits work, writes reports
- **Evaluator Eve** - Runs smoke tests, code review, and edge case testing
- **Nit-pick Nathan** - Extracts missed requirements from the spec and flags violations

Tom orchestrates them in a loop: for each phase, Dan implements, Eve tests, and if all TODOs are resolved, Nathan does a final check. The cycle repeats until the spec is fully satisfied.

## Usage

Pass `TOM.md` as a system prompt to an AI coding agent (e.g. Claude Code) along with a spec file describing what to build. The agent handles the rest.
