# Global Claude Code Instructions

## General Guidelines

- When writing a commit messages, NEVER auto-add your agent name as co-author
- When making technical decisions, do not give much weight to development cost. Instead, prefer quality, simplicity, robustness, scalability, and long-term maintainability.

## Working Style

- Always begin by thinking deeply before you code; explicitly stating your assumptions,surfacing tradeoffs, and halting to ask for clarification the moment you encounter ambiguity
rather than guessing silently.
- Write only the absolute minimum amount of code required to solve the immediate problem strictly avoiding speculative features, unrequested abstractions, or predictive configurations.
- When editing existing code, make highly surgical changes by restricting your updates only
to the exact lines necessary to fulfill the request, maintaining the existing style perfectly, and leaving adjacent, unbroken code completely untouched unless your changes directly orphaned an import or variable.
- Approach every task through goal-driven execution by breaking it down into a clear,step-by-step plan with strong success criteria, such as writing a reproducing or failing test first and independently looping through verification until that specific goal is strictly met.

## Communication

- Be precise.
- Call out trade-offs when multiple reasonable approaches exist.
- Push back if a safer or smaller approach would meet the goal.

## Self-learing

When I correct you, or you catch yourself making a mistake: before continuing, add the lesson as a one-line rule under ## Lessons, so it never happens again.

## Lessons

- (Claude adds rules here)
- Never run `git commit` unless Bac explicitly asks, even when a skill/process says to commit.
