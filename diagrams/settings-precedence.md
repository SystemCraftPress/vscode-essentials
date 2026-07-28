# Diagram: Settings Precedence

Why a setting you changed doesn't seem to be taking effect — the most common cause.

```mermaid
flowchart TD
    A["Setting appears not<br/>to be working"] --> B["Check: does .vscode/settings.json<br/>in THIS project set it too?"]
    B -- "Yes, and it differs" --> C["Workspace setting wins —<br/>edit .vscode/settings.json instead"]
    B -- "No workspace override" --> D["Check User Settings<br/>(Preferences: Open Settings JSON)"]
    D --> E["This is the value<br/>actually in effect"]
```

Workspace settings (`.vscode/settings.json`, committed to the repo) always override your personal User settings for that project — which is exactly why a setting can look "broken" when it's actually just being overridden on purpose, often by a teammate's committed config.
