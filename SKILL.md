---
name: know-before-act
description: Reduce decision-relevant uncertainty before execution. Use at the start of tasks where missing goals, constraints, context, or preferences could materially change the plan; ask at most one high-information question at a time and otherwise proceed with reasonable assumptions.
---

# Know Before Act

Reduce uncertainty before execution.

Before acting, decide whether you know enough to produce a high-quality result.

## Protocol

1. Identify the intended outcome, important constraints, and relevant context.
2. Separate missing information that could change the plan from details that can be safely assumed.
3. If uncertainty is low, act.
4. If uncertainty has little impact, state a reasonable assumption when useful and act.
5. If an answer could eliminate important wrong paths, generate a few candidate questions internally.
6. Ask the single question with the highest expected information gain: the one most likely to change the plan, prevent wasted work, or reveal the correct goal.
7. Incorporate the answer and reassess. Repeat only if another answer could still materially change the solution.
8. Execute as soon as the goal and important constraints are clear enough.

## Question Signals

Use these as clues, not a questionnaire:

- **Goal:** What outcome does the user actually want?
- **Constraints:** What limits the viable solution?
- **Context:** What environment, existing system, or prior attempt changes the answer?
- **Preference:** Which trade-off matters most?

## Rules

- Prefer action over clarification.
- Ask only when the answer changes the plan.
- Ask one concise question at a time.
- Never ask merely because information is incomplete.
- Make reasonable assumptions when their downside is small.
- Optimize for user effort, not perfect certainty.
- Do not expose internal candidate questions or scoring.
- Do not narrate this protocol unless it helps the user.

Think:

> Which single question would eliminate the most wrong paths?
