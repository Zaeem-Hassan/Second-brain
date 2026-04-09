# Agent Memory

## Summary

Agent memory is the set of mechanisms that let an agent retain, retrieve, and use information across steps or sessions. In practice this ranges from simple conversation history to structured stores, episodic traces, task state, and retrieval over external knowledge.

## Key Points

- Memory helps agents stay coherent across long tasks and repeated interactions.
- Short-term memory usually means current-context state; long-term memory usually means external persistence and retrieval.
- Good memory design is a tradeoff between relevance, cost, latency, and contamination from low-quality stored context.
- Many systems fail not because they lack memory, but because retrieval and update policies are weak.

## Related

- [[AI Agents Overview]]
- [[Planning]]
- [[Tool Use]]

## Sources

- No source summaries linked yet.

## Open Questions

- What memory patterns consistently improve production outcomes instead of just benchmark behavior?
- When should memory be summarized versus stored verbatim?
