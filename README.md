<div align="center">

# 🎨 Claude Artefacts

**Витрина HTML-артефактов, собранных в паре с [Claude Code](https://claude.com/claude-code).**

[![Live](https://img.shields.io/badge/live-grafsoul.github.io-d97757?style=flat-square)](https://grafsoul.github.io/claude-artefacts/)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-main%20%2F%20docs-1c1917?style=flat-square&logo=github)](https://github.com/GrafSoul/claude-artefacts/settings/pages)
![Zero deps](https://img.shields.io/badge/dependencies-0-4d7c4a?style=flat-square)

[**Открыть витрину →**](https://grafsoul.github.io/claude-artefacts/)

</div>

---

## Как устроено

Один статичный лендинг, который сам собирает список из реестра. Никакой сборки, фреймворков и зависимостей — чистый HTML + немного JS.

```
docs/
├── index.html      # витрина: читает manifest.json, рисует карточки, тема light/dark
├── manifest.json   # реестр артефактов — единственное, что правится при добавлении
└── <artefact>.html # сами артефакты, по файлу на каждый
```

> [!NOTE]
> `index.html` ничего не хардкодит. Добавить артефакт = положить HTML в `docs/` и дописать **одну запись** в `manifest.json`. Разметку витрины трогать не нужно.

---

## Добавить артефакт

**1.** Кладём файл в `docs/`, например `docs/revenue-dashboard.html`
**2.** Дописываем объект в массив `artefacts` внутри `manifest.json`:

```json
{
  "title": "Revenue Dashboard",
  "description": "Интерактивный дашборд выручки по кварталам",
  "path": "revenue-dashboard.html",
  "emoji": "📊",
  "date": "2026-07-15",
  "tags": ["react", "chart"]
}
```

| Поле          |                 | Описание                    |
| ------------- | --------------- | --------------------------- |
| `title`       | **обязательно** | Название на карточке        |
| `path`        | **обязательно** | Имя файла внутри `docs/`    |
| `description` | опц.            | Одна строка о сути          |
| `emoji`       | опц.            | Иконка карточки             |
| `date`        | опц.            | Дата в формате `YYYY-MM-DD` |
| `tags`        | опц.            | Массив меток-чипов          |

---

## Публикация

Витрина отдаётся через **GitHub Pages**:

```
https://grafsoul.github.io/claude-artefacts/
```

> [!IMPORTANT]
> Pages включается один раз вручную: **Settings → Pages → Source: `main` / `/docs`**.

---

<div align="center">
<sub>Собрано в паре с Claude Code · без зависимостей, без сборки</sub>
</div>
