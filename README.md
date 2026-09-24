# mdfit - Fit Any Markdown

An Obsidian plugin that auto-converts pasted LLM output (ChatGPT / Claude /
Gemini) into clean Markdown the moment it lands in a note — no manual cleanup.

Paste from an AI chat and get, instantly:

- Math that renders: `\(...\)` → `$...$`, `\[...\]` → `$$...$$`, LaTeX
  environments wrapped, mid-sentence display math kept on its own lines.
- Correct heading levels (ChatGPT's shallow `###` headings promoted to `#`).
- Citation noise like `【20†L33-L40】` and dangling `[1]` stripped.
- Real Markdown tables and task lists recovered from chat-app HTML.
- `**Note:**` paragraphs turned into Obsidian callouts.
- Tidy CJK ↔ Latin spacing, zero-width characters and "Copy code" junk removed.

Code blocks, inline code and math are never touched — conversion is guarded by
a protection layer, so examples inside your notes stay byte-identical.

## Usage

Just paste into any note (`Ctrl+V`). The plugin converts the clipboard content
(plain text, or the rich HTML flavor when it carries tables/KaTeX) and inserts
the result. Toggle it at any time with the command
**"mdfit: Toggle paste conversion on/off"**.

## Install

### From the community directory (recommended)

Settings → Community plugins → Browse → search **"mdfit"** → Install.

### Manual install

1. Download `main.js` and `manifest.json` from the
   [latest release](https://github.com/Naloam/mdfit-obsidian-plugin/releases/latest).
2. Copy both files into `<your-vault>/.obsidian/plugins/mdfit/`.
3. Enable **mdfit - Fit Any Markdown** in Settings → Community plugins.

## Development

The source code lives in the
[md-fit-all monorepo](https://github.com/Naloam/md-fit-all/tree/main/packages/obsidian-plugin)
(`packages/obsidian-plugin`), alongside the `mdfit` CLI and the conversion
engine `mdfit-core`. This repository is the release channel for the Obsidian
community directory.

MIT License.
