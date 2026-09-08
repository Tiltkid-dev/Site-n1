# Tiltkid — Web Developer · Cypher

A dark English/Persian personal portfolio built with HTML, CSS and vanilla JavaScript, with room for new projects, independent hosting and a future React migration.

**[Live website](https://tiltkid-portfolio.tiltkid.chatgpt.site)** · **[راهنمای فارسی](docs/README.fa.md)** · **[Development](docs/DEVELOPMENT.md)** · **[Hosting & domains](docs/DEPLOYMENT.md)**

## Features

- Five separate tabs: Home, Work, Services, About and Contact.
- English by default, Persian RTL, and a device-local language preference.
- Shareable section links, browser history and keyboard navigation.
- Responsive dark design, user-supplied portrait and reduced-motion support.
- Flowboard task manager, Chroma Studio palette tool and Sentinel network simulation.
- Telegram, X, GitHub and email links.
- A placeholder for the owner's existing attendance software, awaiting real project material.

## Status and authorship

Created for Tiltkid with ChatGPT/Codex assistance. The three interactive projects are concept demos, not commissioned client work. The attendance application's source is **not included**; only its pending portfolio entry exists here. “Cypher” is a creative brand descriptor, not a certification.

There is no backend, database, dependency installation or build step. **`dist/` contains the authored source, not disposable build output. Keep it tracked in Git.** The current application is not React.

## Get the code

```bash
git clone https://github.com/Tiltkid-dev/Site-n1.git
cd Site-n1
```

Or use **Code → Download ZIP** on GitHub and extract it.

## Run locally

Install Python 3.9 or newer and run this from the repository root:

```bash
python3 -m http.server 8000 --bind 127.0.0.1 --directory dist
```

On Windows with the Python launcher:

```powershell
py -m http.server 8000 --bind 127.0.0.1 --directory dist
```

Open `http://localhost:8000`. Stop with `Ctrl+C`. This is a local development server, not production hosting.

## Repository map

| Path | Purpose |
| --- | --- |
| `dist/index.html` | Structure, English text, project cards, contact links and dialogs |
| `dist/style.css` | Theme, typography, mobile/desktop and RTL layouts |
| `dist/app.js` | Persian translations, language switch, demos and tabs |
| `dist/assets/` | Portrait and favicon; add future project images here |
| `docs/DEVELOPMENT.md` | Adding projects, translations and sections |
| `docs/DEPLOYMENT.md` | Static hosting, GitHub Pages and custom domains |
| `docs/ROADMAP.md` | Future ideas, separate from current functionality |
| `docs/README.fa.md` | Persian setup and maintenance guide |
| `scripts/check.py` | Dependency-free structural validation |
| `.github/workflows/pages.yml` | Optional manual GitHub Pages publication |
| `.openai/hosting.json` | Existing managed Sites identity and public directory |
| `CHANGELOG.md` | Milestones |
| `CREDITS.md` | Authorship and asset provenance |

## Demos

| Demo | Working interactions | Boundary |
| --- | --- | --- |
| Flowboard | Add/remove tasks, move stages and reset | Session memory only; reload resets |
| Chroma Studio | Base color, four swatches and CSS export | Local browser download |
| Sentinel | Isolate/reconnect sample devices and reset | Simulation only; no real network access |

Only the language preference uses localStorage. Contact links use mailto or external URLs; there is no message-delivery backend.

## Edit and verify

Update the relevant source, add Persian translations for new text, then run:

```bash
python3 scripts/check.py
node --check dist/app.js
```

Node.js is needed only for the second check. Review both languages, all tabs, mobile layout and any changed demo locally. The checks do not replace browser or visual testing. See the [development guide](docs/DEVELOPMENT.md).

Commit your changes and push to your own repository. Saving code and publishing a live website are separate operations.

## Hosting and growth

A compatible static host can serve `dist/` as the web root. The supplied GitHub Pages workflow runs **only when manually triggered**; storing this repository does not automatically publish another site. Follow [DEPLOYMENT.md](docs/DEPLOYMENT.md) when ready.

No custom domain is configured. New real portfolio projects, a contact backend and a React migration are future options described in the [roadmap](docs/ROADMAP.md).

## Assets and licensing

The portrait was supplied by the owner; broader redistribution rights and its original creator have not been established. Google Fonts supplies Manrope, DM Sans and Vazirmatn at runtime; system fallbacks exist. No open-source license has been selected or blanket license granted for third-party artwork. See [CREDITS.md](CREDITS.md).

## References

- [GitHub Pages workflows](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages)
- [GitHub Pages custom domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)
- [MDN dialog](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog)
- [MDN dir attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/dir)
- [Python local server](https://docs.python.org/3/library/http.server.html)
