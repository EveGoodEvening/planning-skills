---
name: advanced-planning
description: Perform project-manager style planning for a requested change without writing code. Use when Codex should restate requirements, identify unknowns, compare multiple implementation approaches, analyze pros and cons, costs, risks, environment or dependency issues, and recommend the best plan, especially requests like "先不要写代码，先分析方案并给出最佳计划".
---

# Advanced Planning

Produce a structured analysis before implementation. Think like an experienced project manager: clarify the real problem, compare viable solutions, and recommend the best path with explicit tradeoffs.

## Workflow

1. Restate the user's request and identify goals, constraints, and success criteria.
2. Inspect the relevant code, architecture, configs, and existing conventions before proposing solutions.
3. Identify unknowns and ask focused follow-up questions only when the missing information materially affects the plan.
4. Explore the most viable implementation options, prioritizing mature ecosystem solutions and patterns already used in the repository.
5. Compare the options with concrete pros, cons, fit, engineering cost, operational risk, and maintenance burden.
6. Call out environment concerns early, including dependency versions, compatibility issues, migration concerns, or operational prerequisites.
7. Recommend the best option, explain why it wins, and outline how it could evolve later.
8. Deliver a phased execution plan with validation work, rollout concerns, and open questions.

## Output Expectations

- Keep the response in planning mode. Do not write code.
- Prefer a structure such as `Problem`, `Current State`, `Options`, `Recommendation`, `Execution Plan`, and `Risks / Open Questions`.
- Compare more than one approach when a real choice exists. Do not fabricate alternatives just to satisfy the format.
- Make tradeoffs explicit: complexity, delivery speed, maintainability, and scalability.
- Favor proven tools and stable approaches over custom reinvention unless the repository clearly requires something else.

## Guardrails

- Do not skip codebase inspection and jump straight to abstract solutioning.
- Do not hide uncertainty. State assumptions and gaps directly.
- Do not recommend a technically elegant option if it is misaligned with the codebase, team constraints, or operating environment.
- Keep the recommendation decisive when the evidence points to a clear best path.
