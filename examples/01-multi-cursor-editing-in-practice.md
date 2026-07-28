# Example: Multi-Cursor Editing in Practice

A worked example of the edit that feels like magic the first time and routine forever after.

## The Scenario

You have a list of variable declarations that all need the same prefix added:

```javascript
name = "Ada";
age = 32;
role = "Engineer";
active = true;
```

You want:

```javascript
const name = "Ada";
const age = 32;
const role = "Engineer";
const active = true;
```

## The Slow Way

Click at the start of each line, type `const `, four separate times. Fine for four lines. Painful for forty.

## The Multi-Cursor Way

**Step 1:** Click at the start of the first line.

**Step 2:** Add a cursor at the start of every other line: `Ctrl+Alt+Down` (Win/Linux) or `Cmd+Option+Down` (Mac), three times.

**Step 3:** Type `const ` once. It's inserted at all four cursor positions simultaneously.

## A Second Pattern: Select Next Occurrence

Different problem: rename every instance of a specific variable, but only within this function (not project-wide, which would call for Rename Symbol instead).

**Step 1:** Double-click the first instance of the word to select it.

**Step 2:** Press `Ctrl+D` (Win/Linux) or `Cmd+D` (Mac) repeatedly — each press adds the *next* matching occurrence to your selection.

**Step 3:** Type the replacement. Every selected occurrence updates at once.

## Knowing When to Use Which

| Situation | Tool |
|---|---|
| Same edit at several arbitrary cursor positions | `Ctrl+Alt+Up/Down` (add cursor above/below) |
| Renaming a real code symbol (variable, function) everywhere it's used | `F2` Rename Symbol — see [Example 2](02-project-wide-search-and-replace.md) |
| Replacing a specific word, locally, occurrence by occurrence | `Ctrl+D` Select Next Occurrence |
| Same replacement everywhere, whole project | Find & Replace across project |

Multi-cursor editing is for editing multiple places at once by hand — the moment you're renaming a real symbol used across files, `F2` is the correct tool, not multi-cursor.

See the [cheat sheet](../cheatsheet/vscode-essentials-cheatsheet.md#editing) for the bare shortcuts.
