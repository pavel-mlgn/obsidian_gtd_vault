# Obsidian + GTD

Готовое хранилище (vault) [Obsidian](https://obsidian.md/) для ведения дел по методике [Getting Things Done](https://ru.wikipedia.org/wiki/Getting_Things_Done). Задачи, проекты, встречи и справочные заметки связаны ссылками, а плагины собирают их в списки задач, дашборды и напоминания.

Как все устроено и почему именно так, подробно разобрано в статье на Хабре [Эффективное ведение дел или Obsidian + GTD](https://habr.com/ru/articles/743628/).

## Быстрый старт

1. Скачайте хранилище: зеленая кнопка **Code** -> **Download ZIP**, затем распакуйте архив в удобную папку. Или через git:
   ```bash
   git clone https://github.com/pavel-mlgn/obsidian_gtd_vault.git
   ```
2. В Obsidian выберите **Open folder as vault** и укажите эту папку.
3. Obsidian спросит, доверяете ли вы автору хранилища. Нажмите **Trust author and enable plugins**, иначе плагины не включатся и дашборды останутся пустыми.
4. Откройте заметку `Dashboards/Todo List`. Это главный дашборд со всеми задачами, проектами и встречами.

## Что внутри

```
Dashboards/    дашборды: задачи, входящие, контакты, ссылки
Demo/          демо-заметки, на которых видно, как все работает
Templates/     шаблоны заметок
Attachments/   вложения: картинки, PDF
.obsidian/     настройки и плагины
```

Каждая заметка относится к одному из пяти типов. Тип задает тег, а новая заметка создается из шаблона в папке `Templates`.

| Тип | Тег | Шаблон | Пример в `Demo` |
| --- | --- | --- | --- |
| Входящие | `#inbox` | `Inbox` | `Idea`, `Plan`, `Thought` |
| Задача | `#task/now`, `#task/next`, `#task/waiting`, `#task/someday` | `Task` | `Task One`, `Task Two`, `Single action` |
| Проект | `#project` | `Project` | `First Project` |
| Встреча | `#meeting` | `Meeting` | `Team Meeting` |
| Справка | `#reference`, `#reference/person`, `#reference/instruction`, `#reference/document` | `Ref-Person`, `Ref-Instruction`, `Ref-Document` | `My Reference`, `@Angela`, `Embed content` |

Дашборды лежат в папке `Dashboards` и собраны в закладках (Bookmarks):
- `Todo List` - активные задачи по статусам, проекты, встречи и последние выполненные задачи;
- `Inbox Notes` - все входящие, которые еще не разобраны;
- `Persons` - таблица контактов;
- `Useful links` - полезные ссылки.

В шапке каждой заметки два запроса Dataview показывают ее исходящие ссылки (OUTGOING) и обратные (BACKLINKS), поэтому отдельные панели ссылок не нужны.

## Плагины

Хранилище использует три плагина сообщества, они уже лежат в `.obsidian/plugins/`:

| Плагин | Зачем |
| --- | --- |
| [Dataview](https://github.com/blacksmithgu/obsidian-dataview) | запросы к заметкам: дашборды, списки задач проекта, ссылки в шапке заметки |
| [Checklist](https://github.com/delashum/obsidian-checklist-plugin) | панель задач и проектов в боковой панели |
| [Reminder](https://github.com/uphy/obsidian-reminder) | напоминания о встречах, дата в формате `@YYYY-MM-DD HH:mm` |

Плагины можно обновить в **Settings -> Community plugins -> Check for updates**.

## Как начать свою систему

Демо-заметки нужны, чтобы посмотреть, как все работает. Когда разберетесь, удалите папку `Demo` и демо-картинки из `Attachments`. Шаблоны, дашборды и настройки останутся, а новые заметки будут создаваться в корне хранилища.

## Лицензия

[MIT](../LICENSE). Плагины в `.obsidian/plugins/` принадлежат их авторам и распространяются по их лицензиям.

---

## In English

A ready-to-use [Obsidian](https://obsidian.md/) vault for task management with the Getting Things Done method. Tasks, projects, meetings and reference notes are linked to each other, and the Dataview, Checklist and Reminder plugins turn them into dashboards, task lists and reminders. The full description is in the [article on Habr](https://habr.com/ru/articles/743628/) (in Russian).

**Quick start.** Download the repository (**Code -> Download ZIP**), open the folder in Obsidian with **Open folder as vault**, click **Trust author and enable plugins**, then open the `Dashboards/Todo List` note. When you are ready to start your own system, delete the `Demo` folder.
