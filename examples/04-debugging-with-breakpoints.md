# Example: A Full Debugging Session

Tracing a real bug using breakpoints and stepping, instead of scattering `console.log` everywhere and rereading output.

## The Bug

A function is supposed to calculate a discount but returns the wrong number for some inputs.

```javascript
function applyDiscount(price, discountPercent) {
  const discount = price * discountPercent;
  return price - discount;
}

applyDiscount(100, 20); // expected 80, got -1900
```

## Step 1: Set a breakpoint

Click in the gutter (left of the line numbers) on the `const discount = ...` line, or place your cursor there and press `F9`. A red dot appears.

## Step 2: Start debugging

Press `F5`. Execution runs normally until it hits the breakpoint, then pauses — the line is highlighted, and execution is frozen at that exact point.

## Step 3: Inspect the variables

With execution paused, hover over `discountPercent` in the editor, or check the Variables panel in the Debug sidebar.

```
price: 100
discountPercent: 20
```

There's the bug: `discountPercent` is `20`, not `0.2`. The function assumes a decimal (`0.2` for 20%) but the caller passed a whole number.

## Step 4: Step over to confirm the effect

Press `F10` (Step Over) to run the `const discount = ...` line and see its result.

```
discount: 2000
```

`100 * 20 = 2000`, not the intended `100 * 0.2 = 20`. Confirmed.

## Step 5: Stop debugging and fix it

`Shift+F5` to stop. Fix the actual bug — either convert the input or fix the calculation, depending on which is the correct contract:

```javascript
function applyDiscount(price, discountPercent) {
  const discount = price * (discountPercent / 100);
  return price - discount;
}
```

## Step Over vs Step Into

If `applyDiscount` had called another function — say, a `roundToTwoDecimals()` helper — `F10` (Step Over) would run that helper without pausing inside it. `F11` (Step Into) would pause at its first line instead. Use Step Into only when you suspect the bug is specifically inside that called function; otherwise Step Over keeps you focused on the code you're actually debugging.

## The Rule

> Step over by default. Step into only when you suspect that specific function.

See the [debugging flow diagram](../diagrams/debugging-flow.md) for the step over/into/out decision as a flowchart.
