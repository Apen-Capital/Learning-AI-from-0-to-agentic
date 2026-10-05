# Domains

The exam has five domains. Task numbering below is `domain.task`.

| # | Domain | Weight |
|---|---|---|
| 1 | Agentic Architecture & Orchestration | 27% |
| 2 | Tool Design & MCP Integration | 18% |
| 3 | Claude Code Configuration & Workflows | 20% |
| 4 | Prompt Engineering & Structured Output | 20% |
| 5 | Context Management & Reliability | 15% |

## 1. Agentic Architecture & Orchestration (27%)

How to build agents that run on their own: the agentic loop, coordinator–subagent systems, and the controls that keep multi-step workflows safe and predictable. The heaviest domain.

- 1.1 Agentic loops: `stop_reason` handling, tool results fed back into the conversation
- 1.2 Multi-agent orchestration with the coordinator–subagent (hub-and-spoke) pattern
- 1.3 Subagent invocation, explicit context passing and spawning (Task tool, `AgentDefinition`)
- 1.4 Multi-step workflows: programmatic enforcement vs prompt guidance, structured handoffs
- 1.5 Agent SDK hooks (`PostToolUse`, call interception) for normalization and compliance
- 1.6 Task decomposition: prompt chaining vs adaptive decomposition
- 1.7 Session state, `--resume` and `fork_session`

## 2. Tool Design & MCP Integration (18%)

How to give agents tools they can choose and use reliably, and how to wire MCP servers into Claude Code and agent workflows.

- 2.1 Tool interfaces: descriptions and clear boundaries
- 2.2 Structured MCP error responses (`isError`, error categories, retryable or not)
- 2.3 Distributing tools across agents and configuring `tool_choice`
- 2.4 MCP servers in Claude Code: `.mcp.json` vs user scope, env var expansion, resources
- 2.5 Built-in tools: Read, Write, Edit, Bash, Grep, Glob

## 3. Claude Code Configuration & Workflows (20%)

How to configure Claude Code for a team and use it day to day, including inside CI/CD pipelines.

- 3.1 `CLAUDE.md` hierarchy, scope and modular organization (`@import`, `.claude/rules/`)
- 3.2 Custom slash commands and skills (frontmatter, `context: fork`, `allowed-tools`)
- 3.3 Path-specific rules for conditional loading of conventions
- 3.4 Plan mode vs direct execution
- 3.5 Iterative refinement: examples, test-driven iteration, the interview pattern
- 3.6 CI/CD integration: `-p`, `--output-format json`, `--json-schema`, independent review

## 4. Prompt Engineering & Structured Output (20%)

How to get consistent, machine-readable output from Claude and keep its quality high at scale.

- 4.1 Explicit criteria to improve precision and cut false positives
- 4.2 Few-shot prompting for consistency
- 4.3 Structured output with tool use and JSON schemas
- 4.4 Validation, retry and feedback loops for extraction quality
- 4.5 Batch processing (Message Batches API: cost, latency, `custom_id`)
- 4.6 Multi-instance and multi-pass review architectures

## 5. Context Management & Reliability (15%)

How to keep agents accurate over long sessions and big inputs, and how they should fail, escalate and cite sources.

- 5.1 Preserving critical information in long conversations
- 5.2 Escalation patterns and resolving ambiguity
- 5.3 Error propagation in multi-agent systems
- 5.4 Context management when exploring large codebases
- 5.5 Human review workflows and confidence calibration
- 5.6 Provenance and uncertainty in multi-source synthesis

## Exam scenarios and their primary domains

Four of these six appear on the exam. They are the material for `Cases/`.

| Scenario | Primary domains |
|---|---|
| 1. Customer Support Resolution Agent | 1, 2, 5 |
| 2. Code Generation with Claude Code | 3, 5 |
| 3. Multi-Agent Research System | 1, 2, 5 |
| 4. Developer Productivity with Claude | 2, 3, 1 |
| 5. Claude Code for Continuous Integration | 3, 4 |
| 6. Structured Data Extraction | 4, 5 |
