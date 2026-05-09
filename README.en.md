# Apex Legends Launch Options Generator

[日本語版 README](./README.md)

A simple, single-file HTML tool for picking Apex Legends launch options via checkboxes, then generating and copying the resulting command-line string. Supports both Japanese and English UI.

Your selections and input values are automatically saved to the browser's `localStorage`, so your settings are restored the next time you open the tool.

## Features

- Options organized by category (Startup / Performance / Resolution / Input / View / Gameplay / Advanced)
- Flag-type options (e.g. `-novid`) are simple checkboxes; value-type options (e.g. `+fps_max 0`) come with a value input
- Each option includes a **description, optional caveat ("Note"), and clickable source links** to EA's official help, the Valve Developer Wiki, PCGamingWiki, and other references
- Paste an existing launch-options string and the tool will auto-tick the options it recognizes and fill in their values
- One-click copy of the generated string to the clipboard
- Selections, input values, and language preference are auto-saved to `localStorage`
- Categories collapse with a click, and each option's details (note + sources) are also collapsible
- Language switcher (JA / EN) in the top-right corner of the header. The initial language is picked based on your browser language
- Responsive layout (desktop, tablet, mobile)

## How to use

Just open `index.html` in a browser. No build step, no dependencies.

```bash
# Example on WSL / Linux
xdg-open index.html

# macOS
open index.html
```

Copy the generated string and paste it into:

- **Steam**: Library → right-click *Apex Legends* → Properties → Launch Options
- **EA app**: Library → click "..." on *Apex Legends* → Properties → Advanced Launch Options

## Hosting on GitHub Pages

This repository can be served directly from GitHub Pages. In the repository's **Settings → Pages**, set the **Source** to the root of the `main` branch and the tool will be published at `https://<username>.github.io/<repo-name>/`.

## References

For primary sources behind each option, see the "Launch options references" section at the bottom of `index.html`. It links to EA's official help pages, the Valve Developer Wiki, PCGamingWiki, the Apex Movement Wiki, ProSettings, and the official Steam community guide.

## Files

- `index.html` — the tool itself (HTML / CSS / JS bundled)
- `README.md` — Japanese README
- `README.en.md` — this file (English)
- `.gitignore`
