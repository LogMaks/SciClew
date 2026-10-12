# SciClew

Научный дискуссионный клуб ([SandBox.Space](https://sandbox.space)). Сайт — статическая витрина на **Jekyll** для **GitHub Pages**.

## Разделы

| Раздел | Путь | Содержание |
|--------|------|------------|
| Главная | `/` | О клубе, темы, как участвовать |
| Встречи | `/meetings/` | Собрания по датам (`_meetings/`) |
| Заметки | `/notes/` | Заметки клуба (`_notes/`) |
| Книги | `/books/` | Источники: ссылки и материалы на сайте (`_books/`) |

## Локальный просмотр

Нужны Ruby и Bundler.

```bash
bundle install
bundle exec jekyll serve
```

Откройте [http://127.0.0.1:4000](http://127.0.0.1:4000).

Сайт на GitHub Pages: [https://logmaks.github.io/SciClew/](https://logmaks.github.io/SciClew/)  
(ветка `Default`, корень; в `_config.yml` — `baseurl: "/SciClew"`).

Локально после `jekyll serve` открывайте http://127.0.0.1:4000/SciClew/

## GitHub Pages

1. **Settings → Pages → Build and deployment → Source:** GitHub Actions *или* Deploy from a branch.
2. Для ветки: выберите ветку (например `Default` / `main`) и папку `/ (root)` — GitHub сам соберёт Jekyll.
3. Плагины ограничены списком GitHub Pages (`jekyll-feed`, `jekyll-seo-tag` уже подключены).

## Структура репозитория

```
_config.yml          # настройки Jekyll
_layouts/            # шаблоны страниц
_includes/           # clew-mark, hero-threads
_meetings/           # коллекция встреч
_notes/              # коллекция заметок
_books/              # коллекция книг/источников
assets/css/          # стили (+ лёгкий CSS-motion)
assets/brand/        # бренд-арт (в т.ч. анонс для Telegram)
index.md             # главная
meetings.md          # список встреч
notes.md             # список заметок
books.md             # список книг
```
