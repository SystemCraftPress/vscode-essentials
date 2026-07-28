# Example: Safe Project-Wide Search and Replace

`Replace All` across an entire project is powerful and, done carelessly, a fast way to break code in files you never looked at. This is the safe sequence.

## The Scenario

Your team renamed a config value from `apiUrl` to `apiBaseUrl`, and it's referenced in a dozen files.

## Step 1: Search first — don't replace yet

`Ctrl+Shift+F` (Win/Linux) / `Cmd+Shift+F` (Mac) — search across the project for `apiUrl`.

Read through the results panel before touching Replace. You're looking for:

- Is `apiUrl` ever part of a *different* identifier, like `apiUrlValidator`, that a naive replace would corrupt into `apiBaseUrlValidator`?
- Is it used in comments or strings where renaming might not actually be correct?
- Is it in a `node_modules` or `vendor` folder that shouldn't be touched at all?

## Step 2: Narrow the search if needed

Use the "files to include / exclude" fields in the search panel. Excluding `node_modules` (usually already excluded by default) and any generated/build folders is worth double-checking before a project-wide replace.

## Step 3: Consider whole-word matching

If `apiUrl` could be a substring of other identifiers, enable "Match Whole Word" in the search panel before proceeding — this prevents `apiUrlValidator` from matching at all.

## Step 4: Enter the replacement, but expand and check a few results first

Type `apiBaseUrl` in the replace field. Before clicking "Replace All," expand a handful of individual results and confirm they look like genuine matches.

## Step 5: Replace All — now that you've actually looked

Only now click Replace All (or replace file-by-file if the change set is small and each one deserves a look).

## When to Reach for Rename Symbol Instead

If `apiUrl` is a real JavaScript/TypeScript identifier — not a string in a config file — `F2` Rename Symbol is usually the better tool. It uses the language server to understand scope, so it won't touch an unrelated `apiUrl` in a different file that happens to share the name but refers to something else entirely.

## The Rule

> Review a project-wide search's matches before clicking Replace All.

See the [multi-cursor example](01-multi-cursor-editing-in-practice.md) for when a smaller-scope edit is the better tool.
