<div align="center">

# 🎨 Claude Artefacts

**A showcase of HTML artefacts built together with [Claude Code](https://claude.com/claude-code).**

[![Live](https://img.shields.io/badge/live-grafsoul.github.io-d97757?style=flat-square)](https://grafsoul.github.io/claude-artefacts/)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-main%20%2F%20docs-1c1917?style=flat-square&logo=github)](https://github.com/GrafSoul/claude-artefacts/settings/pages)
![Zero deps](https://img.shields.io/badge/dependencies-0-4d7c4a?style=flat-square)

[**Open the showcase →**](https://grafsoul.github.io/claude-artefacts/)

</div>

---

## How it works

A single static landing page that builds its own list from a registry. No build step, no frameworks, no dependencies — just plain HTML and a bit of JS.

```
docs/
├── index.html      # showcase: reads manifest.json, renders cards, light/dark theme
├── manifest.json   # artefact registry — the only file you edit to add one
└── <artefact>.html # the artefacts themselves, one file each
```

> [!NOTE]
> `index.html` hardcodes nothing. Adding an artefact = drop an HTML file into `docs/` and append **one entry** to `manifest.json`. The showcase markup stays untouched.

---

## Adding an artefact

**1.** Drop the file into `docs/`, e.g. `docs/revenue-dashboard.html`
**2.** Append an object to the `artefacts` array in `manifest.json`:

```json
{
  "title": "Revenue Dashboard",
  "description": "Interactive quarterly revenue dashboard",
  "path": "revenue-dashboard.html",
  "emoji": "📊",
  "date": "2026-07-15",
  "tags": ["react", "chart"]
}
```

| Field         |              | Description                 |
| ------------- | ------------ | --------------------------- |
| `title`       | **required** | Card heading                |
| `path`        | **required** | File name inside `docs/`    |
| `description` | optional     | One line about what it is   |
| `emoji`       | optional     | Card icon                   |
| `date`        | optional     | Date in `YYYY-MM-DD` format |
| `tags`        | optional     | Array of chip labels        |

---

## Publishing

The showcase is served via **GitHub Pages**:

```
https://grafsoul.github.io/claude-artefacts/
```

> [!IMPORTANT]
> Pages is enabled once, by hand: **Settings → Pages → Source: `main` / `/docs`**.

---

<div align="center">
<sub>Built together with Claude Code · no dependencies, no build step</sub>
</div>
