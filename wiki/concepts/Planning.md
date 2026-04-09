# Planning

## Summary

Planning is the process by which an agent decomposes a goal, selects actions, and updates its approach as new information arrives. It can be explicit, with visible plans and intermediate steps, or implicit within the model's internal reasoning and tool-selection behavior.

## Key Points

- Planning matters most when tasks are long, branching, or require coordination across tools.
- Explicit planning can improve control and observability, but it adds latency and complexity.
- Some tasks benefit more from tight observe-act loops than from detailed up-front plans.
- Better base models may reduce the need for elaborate planning scaffolds, but they do not remove the need for execution control.

## Related

- [[AI Agents Overview]]
- [[Tool Use]]
- [[Agent Memory]]

## Sources

- No source summaries linked yet.

## Open Questions

- When does explicit planning outperform simpler reactive loops in production systems?
- Which planning traces are worth storing as reusable memory artifacts?
