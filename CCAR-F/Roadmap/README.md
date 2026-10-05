# Roadmap

One domain per cycle, four weeks each: two weeks of theory, two of building, closing with a case presentation.

## Cadence

| | |
|---|---|
| Availability | 4h per week |
| Meetings | Monday and Wednesday, 2h each |
| Cycle | 4 weeks, 8 meetings (E1–E8) |
| Domains | 5 |
| Horizon | 22 weeks (20 of cycles, 2 of final review) |

How a cycle works, the four practice-phase models, and what every presentation must deliver: [Cycle-Format.md](Cycle-Format.md).

## The queue

The order follows dependency, not exam weight. Prompt engineering and structured output come first even though they weigh less than agentic architecture: their techniques show up again as correct answers inside the other four domains. Context management and reliability comes last because it only makes sense to instrument a system that already exists.

| Cycle | Weeks | Domain | Owner | Exam weight | Why here |
|---|---|---|---|---|---|
| [1](1-D4-Prompt-Engineering) | 1–4 | D4 Prompt Engineering & Structured Output | Eduardo | 20% (~12 of 60) | Underpins the prompts used in tool descriptions |
| [2](2-D2-Tool-Design-and-MCP) | 5–8 | D2 Tool Design & MCP Integration | Marcus | 18% (~11 of 60) | Feeds the CI configuration in D3 |
| [3](3-D3-Claude-Code) | 9–12 | D3 Claude Code Configuration & Workflows | Marcus | 20% (~12 of 60) | Supplies the tools D1 will orchestrate |
| [4](4-D1-Agentic-Architecture) | 13–16 | D1 Agentic Architecture & Orchestration | Both | 27% (~16 of 60) | Creates the system D5 will instrument |
| [5](5-D5-Context-and-Reliability) | 17–20 | D5 Context Management & Reliability | Eduardo | 15% (~9 of 60) | Instruments what D1 built |
| [6](6-Final-Review) | 21–22 | Closing, no new content | Both | | |

Domain details: [../Domains/README.md](../Domains/README.md).

## Suggested format per domain

To be decided at E4 of each cycle, not now: that is when the size of the case is known. Models A–D are described in [Cycle-Format.md](Cycle-Format.md).

| Domain | Model | Why |
|---|---|---|
| D4 | C | Medium, well-bounded case. One checkpoint is enough |
| D2 | C | Needs a misrouting test before the presentation, so the rehearsal pays off |
| D3 | B | Already used daily. The bottleneck is keyboard time, not doubt |
| D1 | A | Biggest domain and new to both. Justifies all four meetings |
| D5 | B or D | Zero new code, only instrumentation. Use D if D1 ran late |

## Source

Derived from the Claude Certified Architect – Foundations Exam Guide v1.0, July 2026. Domain weights are converted to question counts over a total of 60, so the numbers are approximate. Check flag syntax, paths and frontmatter against docs.claude.com before turning anything here into study material.
