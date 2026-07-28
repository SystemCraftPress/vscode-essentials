# VS Code Quick Reference

Shortcut and command lookup tables for daily VS Code use, Win/Linux and Mac side by side. From the [VS Code Essentials Companion Guide](../README.md).

## Command Palette & Navigation

| Task | Win/Linux | Mac |
|------|-----------|-----|
| Command Palette | `Ctrl+Shift+P` | `Cmd+Shift+P` |
| Quick Open (go to file) | `Ctrl+P` | `Cmd+P` |
| Go to symbol in file | `Ctrl+Shift+O` | `Cmd+Shift+O` |
| Go to symbol in project | `Ctrl+T` | `Cmd+T` |
| Go to line | `Ctrl+G` | `Cmd+G` |
| Go to Definition | `F12` | `F12` |
| Go to References | `Shift+F12` | `Shift+F12` |

## Editing

| Task | Win/Linux | Mac |
|------|-----------|-----|
| Add cursor at click | `Alt+Click` | `Option+Click` |
| Add cursor above/below | `Ctrl+Alt+Up/Down` | `Cmd+Option+Up/Down` |
| Select next occurrence | `Ctrl+D` | `Cmd+D` |
| Copy line up/down | `Shift+Alt+Up/Down` | `Shift+Option+Up/Down` |
| Move line up/down | `Alt+Up/Down` | `Option+Up/Down` |
| Expand selection | `Shift+Alt+Right` | `Shift+Option+Right` |
| Fold region | `Ctrl+Shift+[` | `Cmd+Option+[` |
| Unfold region | `Ctrl+Shift+]` | `Cmd+Option+]` |
| Format document | `Shift+Alt+F` | `Shift+Option+F` |
| Rename symbol | `F2` | `F2` |
| Quick Fix | `Ctrl+.` | `Cmd+.` |

## Search & Replace

| Task | Win/Linux | Mac |
|------|-----------|-----|
| Find in file | `Ctrl+F` | `Cmd+F` |
| Replace in file | `Ctrl+H` | `Cmd+Option+F` |
| Find across project | `Ctrl+Shift+F` | `Cmd+Shift+F` |

## Panels & Views

| Task | Win/Linux | Mac |
|------|-----------|-----|
| Toggle terminal | `` Ctrl+` `` | `` Cmd+` `` |
| Toggle side bar | `Ctrl+B` | `Cmd+B` |
| Explorer | `Ctrl+Shift+E` | `Cmd+Shift+E` |
| Search | `Ctrl+Shift+F` | `Cmd+Shift+F` |
| Source Control | `Ctrl+Shift+G` | `Cmd+Shift+G` |
| Run and Debug | `Ctrl+Shift+D` | `Cmd+Shift+D` |
| Extensions | `Ctrl+Shift+X` | `Cmd+Shift+X` |

## Debugging

| Task | Win/Linux | Mac |
|------|-----------|-----|
| Start debugging / continue | `F5` | `F5` |
| Toggle breakpoint | `F9` | `F9` |
| Step over | `F10` | `F10` |
| Step into | `F11` | `F11` |
| Step out | `Shift+F11` | `Shift+F11` |
| Stop debugging | `Shift+F5` | `Shift+F5` |

## Quick Open Prefixes

| Prefix | Searches |
|--------|----------|
| *(nothing)* | Files by name |
| `>` | Commands (Command Palette) |
| `@` | Symbols in the current file |
| `#` | Symbols across the project |
| `:` | Line number |

## Useful Command Palette Entries

| Command | Purpose |
|---------|---------|
| `Preferences: Open Settings (JSON)` | Edit `settings.json` directly |
| `Preferences: Open Keyboard Shortcuts (JSON)` | Edit `keybindings.json` directly |
| `Tasks: Run Task` | Run a task from `tasks.json` |
| `Git: Create Branch` | Create and switch to a new branch |
| `Terminal: Select Default Profile` | Change the default shell |
| `Developer: Reload Window` | Reload VS Code without restarting |
| `Extensions: Show Recommended Extensions` | See extensions the project suggests |

## Key Configuration Files

| File | Purpose |
|------|---------|
| `.vscode/settings.json` | Workspace-level settings |
| `.vscode/tasks.json` | Saved, runnable commands |
| `.vscode/launch.json` | Debug configurations |
| `.vscode/extensions.json` | Recommended extensions for the project |
| `keybindings.json` | Personal keyboard shortcut overrides |

---

For the "why" behind these — plus source control and extension workflows — see the [VS Code Essentials Companion Guide](../README.md#get-the-full-companion-guide).
