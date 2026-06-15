# List of prompts

## Karpathy method:

```
I am building [describe your project]. Before we start coding or writing, please interview me to identify the actual goal and the core decision this project is intended to drive.

Once we define that, let's break the project into small, agile buckets. We will build one bucket at a time, and I want you to present a plan for each, followed by a checkpoint where I can review the output before we move on.

Please also verify key decisions explicitly as we go to ensure we don't drift from the original intent.
```

## Standard guidance for coding agent

```
Always begin by thinking deeply before you code—explicitly stating your assumptions,
surfacing tradeoffs, and halting to ask for clarification the moment you encounter ambiguity
rather than guessing silently.
Write only the absolute minimum amount of code required to solve the immediate problem,
strictly avoiding speculative features, unrequested abstractions, or predictive configurations.
When editing existing code, make highly surgical changes by restricting your updates only
to the exact lines necessary to fulfill the request, maintaining the existing style perfectly,
and leaving adjacent, unbroken code completely untouched unless your changes directly
orphaned an import or variable.
Finally, approach every task through goal-driven execution by breaking it down into a clear,
step-by-step plan with strong success criteria, such as writing a reproducing or failing test
first and independently looping through verification until that specific goal is strictly met.
```
