# Exercise 2: Configure a Custom Task

**Goal:** write a `tasks.json` from scratch for a real command you actually run, following the pattern from [Example 3](../../examples/03-a-tasks-json-workflow.md).

**Time:** ~15 minutes

## Task

Pick a command you currently type manually and repeatedly in your own project — a build command, a linter, a test runner, anything real. If you don't have one handy, use this practice command:

```bash
echo "Running checks..." && sleep 1 && echo "All checks passed."
```

1. Create `.vscode/tasks.json` in a test project (via the Command Palette, not by hand-typing the whole file from memory).
2. Define a task with a clear `label` for your chosen command.
3. Set `presentation.panel` to `"dedicated"` so repeated runs reuse the same terminal panel.
4. Run it via `Tasks: Run Task` from the Command Palette.
5. Make it the default build or test task (via `group.isDefault`) and run it with the corresponding keyboard shortcut instead.

## Checkpoints

- [ ] `tasks.json` is valid JSON — VS Code doesn't show a red squiggle or an error when you open it
- [ ] Running the task via `Tasks: Run Task` produces output in the integrated terminal
- [ ] Running it a second time reuses the same terminal panel, not a new one
- [ ] You can run it via the default-task keyboard shortcut, not just from the Command Palette

## Stretch Goal

Add a second task, and set up `dependsOn` so running the first task automatically runs the second one after it completes.

## Reference

See the [tasks.json example](../../examples/03-a-tasks-json-workflow.md) and the [key configuration files table](../../reference/quick-reference.md#key-configuration-files).
