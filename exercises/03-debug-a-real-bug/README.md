# Exercise 3: Debug a Real Bug

**Goal:** use breakpoints and stepping to find a bug, instead of `console.log`/`print` statements — the workflow from [Example 4](../../examples/04-debugging-with-breakpoints.md).

**Time:** ~20 minutes

## Setup

Use this small, deliberately buggy function (any language with VS Code debugger support works — this is written in JavaScript, adapt as needed):

```javascript
function calculateAverage(numbers) {
  let total = 0;
  for (let i = 0; i <= numbers.length; i++) {
    total += numbers[i];
  }
  return total / numbers.length;
}

console.log(calculateAverage([10, 20, 30])); // expect 20, get NaN
```

## Task

1. Set a breakpoint inside the `for` loop, on the `total += numbers[i]` line.
2. Start debugging (`F5`) and let it hit the breakpoint.
3. Use Step Over (`F10`) repeatedly, watching the `total` and `i` variables in the Debug sidebar after each step.
4. Identify the exact iteration where something goes wrong — what is `numbers[i]` on that iteration, and why?
5. Stop debugging, fix the bug, and re-run to confirm the output is now `20`.

## Checkpoints

- [ ] You identified the off-by-one error (`<=` instead of `<`) by watching variable values, not by reading the code and guessing
- [ ] You can explain what `numbers[i]` evaluates to on the failing iteration and why that produces `NaN`
- [ ] After your fix, `calculateAverage([10, 20, 30])` returns `20`

## Stretch Goal

Add a watch expression (in the Debug sidebar's Watch panel) for `numbers[i]` before you start stepping, so its value updates automatically at each breakpoint pause instead of you checking it manually each time.

## Reference

See the [debugging example](../../examples/04-debugging-with-breakpoints.md) and the [debugging flow diagram](../../diagrams/debugging-flow.md).
