# Know Before Act

[![skills.sh](https://skills.sh/b/yj972/know-before-act)](https://skills.sh/yj972/know-before-act/know-before-act)

Know Before Act is a lightweight agent protocol that reduces uncertainty before execution by asking high-information questions.

Agents often either act too early or ask too much. This protocol adds one small decision before execution: act when the path is clear; otherwise ask the single question most likely to change it.

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
