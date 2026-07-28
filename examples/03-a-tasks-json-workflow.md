# Example: A Real `tasks.json` Workflow

Turning a command you type repeatedly into something you run with a keyboard shortcut instead.

## The Scenario

You keep typing `npm run test -- --watch` manually every time you start working. Time to make it a task.

## Step 1: Create the task

Open the Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`) and run `Tasks: Configure Task` → `Create tasks.json file from template` → `Others`. This creates `.vscode/tasks.json`.

## Step 2: Define it

```json
{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "test:watch",
      "type": "shell",
      "command": "npm run test -- --watch",
      "group": {
        "kind": "test",
        "isDefault": true
      },
      "presentation": {
        "reveal": "always",
        "panel": "dedicated"
      },
      "problemMatcher": []
    }
  ]
}
```

## Step 3: Run it

Command Palette → `Tasks: Run Task` → `test:watch`. Because it's set as the default test task, you can also just press `Ctrl+Shift+B` in many setups, or bind a custom shortcut to `workbench.action.tasks.test`.

## What Each Field Actually Does

- **`label`** — the name you'll see and select from `Tasks: Run Task`.
- **`command`** — the actual shell command, exactly as you'd type it in the terminal.
- **`group.isDefault`** — makes this the task that runs when you use the default test-task shortcut, instead of having to pick it from a list every time.
- **`presentation.panel: "dedicated"`** — reuses the same terminal panel each run instead of spawning a new one, so a long-running watch task doesn't pile up terminal tabs.

## Committing It

`.vscode/tasks.json` is meant to be committed to the repo — that's the point. Anyone who clones the project gets the same runnable task, not just you.

See the [key configuration files table](../reference/quick-reference.md#key-configuration-files) for what the other `.vscode/*.json` files are for.
