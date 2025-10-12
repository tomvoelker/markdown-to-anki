# Markdown to Anki HTML Converter

> A simple, vibecoded tool I built for myself to stop fighting with markdown → Anki conversions

## What is this?

I got tired of LLMs spitting out perfectly good markdown study materials that Anki just couldn't handle. This tool fixes that by converting markdown (with LaTeX math) into Anki's specific HTML format.

It's a single-page app that does everything client-side. No server, no dependencies, no BS.

## Features

- **Single Card Mode**: Convert one card at a time with live preview
- **Batch Mode**: Process multiple Q&A pairs at once
- **Auto-copy**: Results copied to clipboard automatically
- **Full LaTeX Support**: Inline `\(x\)` or `$x$`, block `\[x\]` or `$$x$$`, even `\begin{align*}...\end{align*}`
- **Smart Lists**: Markdown lists → proper HTML `<ul>`/`<ol>` with sub-items
- **Keyboard Shortcuts**: `Ctrl/Cmd+K` to clear, `Esc` to close info

## Quick Start

Just open `index.html` in your browser. That's it.

Or use it online: [Live Demo](https://tomvolker.github.io/markdown-to-anki) *(if hosted)*

## Conversions

| Markdown | Anki HTML |
|----------|-----------|
| `**bold**` or `__bold__` | `<b>bold</b>` |
| `*italic*` or `_italic_` | `<b>italic</b>` |
| `\(x^2\)` or `$x^2$` | `<anki-mathjax>x^2</anki-mathjax>` |
| `\[E=mc^2\]` or `$$E=mc^2$$` | `<anki-mathjax block="true">E=mc^2</anki-mathjax>` |
| `- item` | `<ul><li>item</li></ul>` |
| `1. item` | `<ol><li>item</li></ol>` |

## Batch Mode Format

```
```
Your question here with **bold** and \(math\)
```

```
Your answer here
```

-----

```
Next question
```

```
Next answer
```
```

Separate cards with `-----` (5 dashes).

## Why?

Because copying markdown from ChatGPT/Claude into Anki was driving me nuts. Built this in a few hours with Claude's help. It works for me, hope it works for you too. 🤷‍♂️

## Technical Details

- Pure HTML/CSS/JavaScript
- MathJax 3 for preview rendering
- Client-side only (your data never leaves your browser)
- No build process, no npm, no webpack, just open the file

## Disclaimer

This tool is provided as-is, vibecoded for personal use. Always review your cards before importing to Anki. Not affiliated with Anki or Damien Elmes.

## License

MIT - do whatever you want with it
