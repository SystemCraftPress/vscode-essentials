# Diagram: Step Over vs Step Into vs Step Out

The decision from [Example 4](../examples/04-debugging-with-breakpoints.md).

```mermaid
flowchart TD
    A["Paused at a breakpoint"] --> B{"Does this line call<br/>another function?"}
    B -- "No" --> C["F10 Step Over —<br/>runs this line, pauses at next"]
    B -- "Yes" --> D{"Do you suspect the bug<br/>is inside that function?"}
    D -- "No" --> C
    D -- "Yes" --> E["F11 Step Into —<br/>pauses at the first line<br/>inside the called function"]
    E --> F{"Done inspecting,<br/>want to return?"}
    F -- "Yes" --> G["Shift+F11 Step Out —<br/>finishes the function,<br/>pauses back in the caller"]
```

Defaulting to Step Over and only stepping into functions you specifically suspect keeps a debugging session focused — stepping into every single function call quickly buries you in code that isn't the problem.
