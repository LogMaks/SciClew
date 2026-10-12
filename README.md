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

Если сайт публикуется как *project site* (`username.github.io/SciClew`), в `_config.yml` задайте:

```yaml
baseurl: "/SciClew"
url: "https://username.github.io"
```

## GitHub Pages

1. **Settings → Pages → Build and deployment → Source:** GitHub Actions *или* Deploy from a branch.
2. Для ветки: выберите ветку (например `Default` / `main`) и папку `/ (root)` — GitHub сам соберёт Jekyll.
3. Плагины ограничены списком GitHub Pages (`jekyll-feed`, `jekyll-seo-tag` уже подключены).

## Структура репозитория

```
_config.yml          # настройки Jekyll
_layouts/            # шаблоны страниц
_meetings/           # коллекция встреч
_notes/              # коллекция заметок
_books/              # коллекция книг/источников
assets/css/          # стили
index.md             # главная
meetings.md          # список встреч
notes.md             # список заметок
books.md             # список книг
```
