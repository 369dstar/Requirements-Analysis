# Requirements Analysis

> A structured requirement analysis workflow that transforms vague ideas into clear, actionable task lists.

## Overview

This project defines an **AI-driven requirement analysis workflow** (implemented as a WorkBuddy Skill). Instead of making decisions for you, it uses a structured questioning framework to help you refine fuzzy ideas into well-defined, executable tasks — while accumulating reusable experience along the way.

## Core Philosophy

- **AI structures the questions** — A fixed framework (5W1H + Socratic probing) ensures nothing falls through the cracks.
- **You make the decisions** — All judgments and choices remain in your hands.
- **Experience is reusable, context is not** — Methodology carries across projects; specific conclusions don't.

## Workflow

The skill operates through six phases:

### Phase 0 — Experience Retrieval (Pre-check)
Searches the "需求分析经验库" (Requirement Analysis Experience Library) notebook for similar past cases. If a highly similar case is found, its methodology is extracted and referenced — but never its specific conclusions.

### Phase 1 — 5W1H Initial Breakdown
Captures the full contour of a requirement in one pass using the 5W1H framework:

| Dimension | Focus | Key Questions |
|-----------|-------|---------------|
| **What** | What to do | Core functionality? Deliverable? Scope boundaries? |
| **Why** | Why | What pain point? What goal? What happens if not done? |
| **Who** | Who's involved | Who uses it? Who decides? Stakeholders? |
| **When** | Timeline | When needed? Hard deadline? Priority? |
| **Where** | Environment | Usage scenario? Deployment? Platform/device? |
| **How** | How | Technical constraints? Resource limits? Preferences? |

### Phase 2 — Socratic Iterative Probing
Drills into ambiguous points identified in Phase 1 using targeted questioning strategies:

- **Purpose tracing** — When the "why" behind a "what" is unclear
- **Boundary testing** — When scope is fuzzy
- **Constraint validation** — When limitations are stated
- **Alternative exploration** — When a solution may be over-engineered
- **Priority sorting** — When there are too many requirements

### Phase 3 — Choice-Based Decision Support
Reduces decision cost by presenting multiple-choice questions with pros/cons for each option and a recommended choice.

### Phase 4 — Task List Production
Converts clarified requirements into structured, executable tasks with:
- Clear subjects and acceptance criteria
- Dependency relationships between tasks
- Priority-ordered排列

### Phase 5 — Experience Sedimentation & Reset
After user confirmation, the analysis is saved as a structured case study in the experience library. Context is then cleared to welcome the next requirement with a blank slate.

## Trigger Conditions

The workflow activates when users express intent with phrases like:

- "I want to..." / "I need to..." / "Help me design..."
- "How to implement..." / "What's the approach for..."
- "Design a..." / "Plan a..." / "Analyze..."
- "Choose between A and B..."
- "Requirement analysis" / "Break down tasks" / "Feature design"

### Incremental Modification (In-Session)

When the skill is already running, it detects modification signals and adjusts accordingly:

| Signal | Example | Action |
|--------|---------|--------|
| **Add** | "Also add..." / "Plus..." | Return to Phase 1 for the new feature |
| **Modify** | "Change..." / "Adjust..." | Return to Phase 2 to confirm intent |
| **Replace** | "Switch to..." / "Use another approach" | Return to Phase 3 for re-evaluation |
| **Remove** | "Remove..." / "Never mind..." | Confirm impact scope, update tasks |
| **Restart** | "Start over..." / "Rethink..." | Return to Phase 0 from scratch |

## Behavioral Guidelines

1. **No repeated questions** — Review conversation history before asking.
2. **Progressive depth** — Start broad, go deep gradually.
3. **Opinionated recommendations** — Every question comes with AI analysis and a suggested option.
4. **Timely convergence** — Move to task breakdown when requirements are clear.
5. **Chinese-first** — All conversations and outputs in Simplified Chinese.
6. **Mandatory confirmation** — Always ask "Is the requirement analysis complete?" after Phase 4.
7. **Experience-first** — Search the experience library before every analysis.
8. **Concise cases** — Each saved case stays under 200 lines.

### Context Isolation (Core Principle)

- Each requirement is an independent project; context does not leak across projects.
- Experience reuse is limited to **methodology** only — never specific conclusions.
- Project A's tech stack, data schema, or business logic is **never** automatically applied to Project B.
- After completing a requirement, context is cleared completely.

## Usage

This skill is designed for use with [WorkBuddy](https://www.codebuddy.cn/docs/workbuddy/Overview). To use it:

1. Place `SKILL.md` in your WorkBuddy skills directory.
2. Start a conversation with any requirement-related prompt (e.g., "I want to build a...").
3. The workflow activates automatically and guides you through the phases.

## File Structure

```
.
├── SKILL.md      # Skill definition (workflow rules, triggers, phases)
└── README.md     # This file
```

## License

This project is shared publicly for reference and educational purposes.
