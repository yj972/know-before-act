# Know Before Act

[![skills.sh](https://skills.sh/b/yj972/know-before-act)](https://skills.sh/yj972/know-before-act/know-before-act)

Know Before Act is a lightweight agent protocol that reduces uncertainty before execution by asking high-information questions.

Agents often either act too early or ask too much. This protocol adds one small decision before execution: act when the path is clear; otherwise ask the single question most likely to change it.

## Theoretical Background

Know Before Act treats clarification as a **conditional POMDP** over a conversation:

- The hidden state is the user's actual goal, constraints, context, and preferences.
- The agent maintains a belief over that state, conditioned on the conversation so far.
- It chooses between acting now and asking one question.
- The answer is an observation that updates the belief; asking also costs user effort and time.

The question policy is inspired by **Bayesian Twenty Questions**: choose the question expected to remove the most uncertainty, then update the posterior from the answer. But information gain alone is not enough—the information must be likely to change the action.

In decision-theoretic terms:

```text
Value(question) = expected improvement in the final action − cost to the user
```

Ask only when that value is meaningfully positive. Otherwise, make a reasonable assumption and act.

This framing connects [POMDP planning](https://doi.org/10.1016/S0004-3702(98)00023-X) with [Bayes-optimal Twenty Questions](https://doi.org/10.1239/jap/1331216837), while keeping the implementation as a small behavior protocol.

## Install

```sh
npx skills add yj972/know-before-act
```

Or copy [`KNOW_BEFORE_ACT.md`](KNOW_BEFORE_ACT.md) into an agent's system prompt or instruction set.

## Example

```text
User: Help me choose a database for my app.
Agent: What workload will dominate: relational transactions, flexible documents, or analytics?
User: Relational transactions.
Agent: [Recommends an option using that constraint.]
```

That is the whole project. It is intentionally a behavior primitive, not a framework.

MIT licensed.
