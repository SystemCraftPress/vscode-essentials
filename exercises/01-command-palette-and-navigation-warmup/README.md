# Exercise 1: Command Palette and Navigation Warmup

**Goal:** build the habit of reaching for the keyboard instead of the mouse for the things you do constantly.

**Time:** ~10 minutes

## Setup

Open any real project with a few files in VS Code.

## Task

Do each of these using only the keyboard — no mouse clicks:

1. Open the Command Palette and run `Preferences: Open Settings (JSON)`.
2. Close it. Use Quick Open to jump directly to a specific file by name.
3. From that file, use Quick Open with the `@` prefix to jump to a specific function or symbol within it.
4. Use `Ctrl+Shift+F` / `Cmd+Shift+F` to search for a word you know appears in at least two files.
5. From the search results, jump to one of the matches, then use `Go to Definition` (`F12`) on a function call in that file.
6. Use `Shift+F12` (Go to References) on that same function to see everywhere it's used.
7. Toggle the integrated terminal open and closed with the backtick shortcut.

## Checkpoints

- [ ] You didn't touch the mouse for any of steps 1–7
- [ ] You can explain the difference between what plain Quick Open (`Ctrl+P`), `@` Quick Open, and `#` Quick Open each search
- [ ] `F12` took you to where a function is defined; `Shift+F12` showed you where it's *used*, elsewhere

## Reference

The [cheat sheet](../../cheatsheet/vscode-essentials-cheatsheet.md) and [quick-open prefixes diagram](../../diagrams/quick-open-prefixes.md) cover everything used here.
