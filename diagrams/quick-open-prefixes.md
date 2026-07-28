# Diagram: Quick Open Prefix Routing

`Ctrl+P` / `Cmd+P` opens the same box every time — what it searches depends entirely on the prefix you type.

```mermaid
flowchart TD
    A["Ctrl+P / Cmd+P"] --> B{"Type a prefix?"}
    B -- "(nothing)" --> C["Search files by name"]
    B -- "&gt;" --> D["Search commands<br/>(same as Command Palette)"]
    B -- "@" --> E["Search symbols in<br/>the current file"]
    B -- "#" --> F["Search symbols across<br/>the whole project"]
    B -- ":" --> G["Jump to a line number"]
```

One box, five different search modes — worth knowing all five instead of only ever using the plain file-name search and reaching for other panels for everything else.
