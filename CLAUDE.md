# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

This is an **Obsidian vault**, not a software project. It has no build, lint, or test commands. It is tracked with git (branch `main`) for version history, and the Obsidian Sync core plugin is enabled for device sync. `.gitignore` excludes Obsidian's UI state (`workspace*.json`), cache, `.trash/`, and community plugin code (`main.js`/`styles.css`, which reinstall). Plugin settings (`data.json`) are tracked, so never put API keys in plugin settings without first adding that plugin's `data.json` to `.gitignore`. `.gitattributes` forces LF line endings.

The Obsidian UI is set to Korean, so write note content in Korean unless the user asks otherwise.

## Vault structure

The vault keeps two systems apart: a **project workbench (PARA)** for getting things done, and a **knowledge engine (Zettelkasten)** for ideas that outlive any project.

```
0. Docs/          reference docs for using this vault with Claude Code (its CLAUDE.md is intentionally empty for now)
1. Projects/      PARA: work with a deadline (one subfolder per project)
2. Areas/         PARA: ongoing responsibilities, no deadline
3. Resources/     PARA: reference material by topic
4. Archive/       PARA: inactive items from 1–3 (keeps their original folder names)
5. Zettelkasten/  Notes move 00. Inbox → 10. Literature → 20. Permanent
6. Templates/     `TPL - <type>.md` note templates
7. Attachments/   all non-Markdown files
```

- **Folder rules:** every folder has its own `CLAUDE.md` with its purpose, what goes there, and its rules (frontmatter, file names). Read it before you create or move notes in that folder.
- **Folder numbers:** they are part of the folder names, so keep them in every path and link.
- **Note types:** every note has a `type` property: `project | area | resource | fleeting | literature | permanent | moc`.
- **Linking direction:** project notes may link into Zettelkasten, but Zettelkasten notes never depend on a project. Zettelkasten notes are never archived.
- **Keeping templates in sync:** if you change a folder's frontmatter rules, also change the matching template in `6. Templates/`.

## Working with notes

- Notes are plain Markdown (`.md`) files. Use Obsidian conventions: `[[wikilinks]]` for links between notes, `#tags`, and YAML frontmatter for properties. The Properties and Bases core plugins are enabled, so frontmatter fields are queryable.
- Enabled core plugins that affect file layout: Daily notes, Templates, Canvas (`.canvas` files), Bases (`.base` files), and Bookmarks. Their folder settings in Obsidian are still at defaults (vault root). They are not yet pointed at `6. Templates/` or `7. Attachments/`.
- An `obsidian-vault` MCP server is available. Its tools (search, read, write, patch, move, tags, frontmatter) keep wikilinks consistent when notes are renamed or moved, so prefer them over raw file moves.
- Community plugin: `terminal`, which embeds a terminal and is probably how Claude Code is launched inside Obsidian.

## Don't touch

- `.obsidian/` holds the vault's app config. `workspace.json` is rewritten constantly by Obsidian, so never edit it. Change other config files only when the user asks.
