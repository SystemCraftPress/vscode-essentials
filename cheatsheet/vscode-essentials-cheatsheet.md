# VS Code Essentials Cheat Sheet

A free, printable one-page reference for VS Code. Pulled straight from the [VS Code Essentials Companion Guide](../README.md). Shortcuts shown as **Win/Linux / Mac**.

## Command Palette & Navigation

| Task | Shortcut |
|------|----------|
| Command Palette | `Ctrl+Shift+P` / `Cmd+Shift+P` |
| Quick Open (go to file) | `Ctrl+P` / `Cmd+P` |
| Go to symbol in project | `Ctrl+T` / `Cmd+T` |
| Go to Definition | `F12` |
| Go to References | `Shift+F12` |

## Editing

| Task | Shortcut |
|------|----------|
| Add cursor above/below | `Ctrl+Alt+Up/Down` / `Cmd+Option+Up/Down` |
| Select next occurrence | `Ctrl+D` / `Cmd+D` |
| Move line up/down | `Alt+Up/Down` / `Option+Up/Down` |
| Expand selection | `Shift+Alt+Right` / `Shift+Option+Right` |
| Format document | `Shift+Alt+F` / `Shift+Option+F` |
| Rename symbol | `F2` |
| Quick Fix | `Ctrl+.` / `Cmd+.` |

## Search & Replace

| Task | Shortcut |
|------|----------|
| Find in file | `Ctrl+F` / `Cmd+F` |
| Find across project | `Ctrl+Shift+F` / `Cmd+Shift+F` |
| Replace in file | `Ctrl+H` / `Cmd+Option+F` |

## Panels & Views

| Task | Shortcut |
|------|----------|
| Toggle terminal | `` Ctrl+` `` / `` Cmd+` `` |
| Toggle side bar | `Ctrl+B` / `Cmd+B` |
| Explorer | `Ctrl+Shift+E` / `Cmd+Shift+E` |
| Source Control | `Ctrl+Shift+G` / `Cmd+Shift+G` |
| Run and Debug | `Ctrl+Shift+D` / `Cmd+Shift+D` |
| Extensions | `Ctrl+Shift+X` / `Cmd+Shift+X` |

## Debugging

| Task | Shortcut |
|------|----------|
| Start / continue | `F5` |
| Toggle breakpoint | `F9` |
| Step over / into / out | `F10` / `F11` / `Shift+F11` |
| Stop debugging | `Shift+F5` |

## Key Configuration Files

| File | Purpose |
|------|---------|
| `.vscode/settings.json` | Workspace settings |
| `.vscode/tasks.json` | Saved, runnable commands |
| `.vscode/launch.json` | Debug configurations |
| `.vscode/extensions.json` | Recommended extensions |

## Golden Rules

> Learn the Command Palette first — everything else builds on it.

> Workspace settings override user settings. Check `.vscode/settings.json` before assuming yours are broken.

> Prefer Rename Symbol (`F2`) over Find & Replace for real code symbols.

> Step over by default. Step into only when you suspect that specific function.

> Review a project-wide search's matches before clicking Replace All.

---

Want the reasoning behind every one of these rules — plus source control, extensions, and a full troubleshooting guide? See the [VS Code Essentials Companion Guide](../README.md#get-the-full-companion-guide).
