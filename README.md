# Эффективное ведение дел или Obsidian + GTD

> Оригинал статьи был опубликован на https://habr.com/ru/articles/743628/.
> Репозиторий является дополнением к статье.

Иногда сложно справиться с большим потоком задач и информации, особенно если это касается работы. Поэтому создание персональной базы знаний для своих текущих дел становится весьма актуальным. Но простая фиксация данных не всегда эффективна: легко потеряться в куче заметок. Различные методики помогают правильно организовать процесс. Вместе с тем информация не существует сама по себе, она, как правило, неразрывно связана со всеми нашими проектами, задачами и другими событиями. Если это учитывать, то проще оперировать данными, находить нужные факты. Через задачу легко выйти на связанную с ней информацию или, наоборот, через данные можно найти проект или задачу, в рамках которых они появились. Однако на практике все это будет эффективно работать, если получится создать единую среду для ведения дел и хранения всех связанных с ними данных.

Существующие приложения, как правило, не могут предоставить готовое решение для работы в таком контексте. Приходится придумывать или создавать что-то свое. Самое простое — это начать с каких-то стандартных заметочников, например Evernote или [OneNote, и приспособить их под себя](https://habr.com/ru/companies/billing/articles/294772/). Однако с появлением Roam-подобных программ пришло понимание, что можно создать очень гибкую систему, которую легко настроить под ведение любого вида задач, проектов и хранение различного типа связанной с ними информации. В этой статье познакомимся с примером настройки и практического использования маркдаун-заметочника [Obsidian.md](https://obsidian.md/) совместно с методологией [Getting Things Done](https://ru.wikipedia.org/wiki/Getting_Things_Done) (GTD) Дэвида Аллена.

Все по-разному пытаются управлять своими делами. Чаще всего применяется простой подход: задачи ведутся в to-do-приложении или удерживаются в голове, а связанная с ними информация раскидывается весьма хаотично. Документы хранятся на диске или в облаке, обсуждения — в email или мессенджерах, заметки — на бумаге или в специализированных приложениях, ссылки на ресурсы — в браузере.

Возможны различные комбинации, но очевидно, что такой подход не слишком эффективен. Для ведения дел и хранения связанных данных удобно использовать один инструмент, например Obsidian. Это не обычный заметочник, как OneNote или Evernote, — он относится к Roam-подобным приложениям ([Roam Research](http://roamresearch.com/) с начала 2020 года [задал новый стандарт](https://medium.com/age-of-awareness/the-history-of-roam-research-and-the-roamcult-4c1e1897633d) в классе). Основные отличительные возможности и полезные фишки такого типа приложений:

-   [Ссылки между заметками](https://publish.obsidian.md/help-ru/%D0%A0%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%B0/%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5+%D0%B2%D0%BD%D1%83%D1%82%D1%80%D0%B5%D0%BD%D0%BD%D0%B8%D1%85+%D1%81%D1%81%D1%8B%D0%BB%D0%BE%D0%BA).
    
-   [Обратные ссылки](https://publish.obsidian.md/help-ru/%D0%9F%D0%BB%D0%B0%D0%B3%D0%B8%D0%BD%D1%8B/%D0%9E%D0%B1%D1%80%D0%B0%D1%82%D0%BD%D1%8B%D0%B5+%D1%81%D1%81%D1%8B%D0%BB%D0%BA%D0%B8#:~:text=%D0%9F%D0%BB%D0%B0%D0%B3%D0%B8%D0%BD%20%C2%AB%D0%9E%D0%B1%D1%80%D0%B0%D1%82%D0%BD%D1%8B%D0%B5%20%D1%81%D1%81%D1%8B%D0%BB%D0%BA%D0%B8%C2%BB%20%D0%BF%D0%BE%D0%BA%D0%B0%D0%B7%D1%8B%D0%B2%D0%B0%D0%B5%D1%82%2C,%D0%BE%D0%B1%D1%80%D0%B0%D1%82%D0%BD%D1%8B%D1%85%20%D1%81%D1%81%D1%8B%D0%BB%D0%BE%D0%BA%20%D0%BD%D0%B0%20%D1%82%D0%B5%D0%BA%D1%83%D1%89%D1%83%D1%8E%20%D0%B7%D0%B0%D0%BC%D0%B5%D1%82%D0%BA%D1%83.) (Backlinks).
    
-   Визуализация связей между заметками ([в виде графа](https://publish.obsidian.md/help-ru/%D0%9F%D0%BB%D0%B0%D0%B3%D0%B8%D0%BD%D1%8B/%D0%93%D1%80%D0%B0%D1%84)).
    
-   [Markdown](https://help.obsidian.md/Editing+and+formatting/Basic+formatting+syntax)\-разметка.
    
-   Шаблоны заметок.
    
-   Ежедневные заметки.
    
-   Расширяемость через плагины. 

Благодаря системе прямых и обратных ссылок, а также их визуализации стала возможна сетевая организация заметок вместо иерархической. Эта организация играет ключевую роль в описанном далее решении.

> К Roam-подобным приложениям также относятся [Logseq](https://logseq.com/), [Notion](https://www.notion.so/), [RemNote](https://www.remnote.com/), [Foam](https://foambubble.github.io/foam/), [TiddlyWiki](https://tiddlywiki.com/) и другие — смотрите подробнее:  
> • [What are the best knowledge base systems for personal use?](https://www.slant.co/topics/4962/~knowledge-base-systems-for-personal-use)  
> • [My 2d Brain Networked Notebook App](https://www.notion.so/My-2d-Brain-Networked-Notebook-App-a131b468fc6f43218fb8105430304709)

Основные достоинства приложения Obsidian:

-   Полностью бесплатное для персонального использования.
    
-   Возможна работа в офлайне, данные хранятся локально на диске в текстовом формате.
    
-   Удобный пользовательский интерфейс.
    
-   Много плагинов.
    
-   Большое сообщество.
    
-   Работает на платформах Mac, Windows, Linux, iOS/Android.
    

В качестве методики управления делами будем использовать проверенную временем и до сих пор популярную систему Getting Things Done (GTD) Дэвида Аллена. Для более детального знакомства с GTD рекомендую статьи на Habr:

-   [GTD за 15 минут: прагматическое руководство](https://habr.com/ru/companies/wunderfund/articles/648663/https://habr.com/ru/companies/wunderfund/articles/648663/https://habr.com/ru/companies/wunderfund/articles/648663/https://habr.com/ru/companies/wunderfund/articles/648663/)
    
-   [Исчерпывающее руководство Getting Things Done (GTD) метода с примерами](https://habr.com/ru/articles/599391/)
    
-   [GTD. Мифы, ошибки, заблуждения](https://habr.com/ru/articles/123669/)

## Общая концепция

Для начала рассмотрим общий вид будущего решения. Идея остается прежней — в рамках одного приложения реализовать ведение дел и хранение связанной с ними информации. В качестве управляющей системы использовать GTD.

В Obsidian определяем пять основных типов заметок:

-   **Inbox** — заметка для фиксации идей, мыслей, планов и т. п.
    
-   **Task** — задача. Единичное действие.
    
-   **Project** — проект. Активность, требующая планирования. Состоит из одного и более действий.
    
-   **Meeting** — встреча, собрание, то, что требует напоминания.
    
-   **Reference** — справочные материалы.
    
    ![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/7e7/186/6f6/7e71866f6016aecead3c14f0e301a5b4.png)
    
    Согласно GTD, заметки Inbox являются источником для создания всех других типов заметок. Справочные материалы (Reference) рождаются в процессе работы и связываются с конкретными задачами, проектами или другими элементами.
    

Никакой иерархии не существует, все заметки находятся на одном уровне и связываются между собой через линки.

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/0a4/bae/e53/0a4baee53eaba921653980d7e59dd9f8.png)

Заметки в Obsidian будут создаваться не напрямую, а через шаблоны. Для каждого типа заметки свой шаблон. В нем определяется структура заметки, тег типа и при необходимости дополнительные элементы.

[Тегами](https://publish.obsidian.md/help-ru/%D0%A0%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%B0/%D0%A0%D0%B0%D0%B1%D0%BE%D1%82%D0%B0+%D1%81+%D1%82%D0%B5%D0%B3%D0%B0%D0%BC%D0%B8) типов заметок будут inbox, project, task и т. д. Для некоторых типов, например для task или reference, добавляются подтипы (через [вложенные теги](https://publish.obsidian.md/help-ru/%D0%9F%D0%BB%D0%B0%D0%B3%D0%B8%D0%BD%D1%8B/%D0%9F%D0%B0%D0%BD%D0%B5%D0%BB%D1%8C+%D1%82%D0%B5%D0%B3%D0%BE%D0%B2#%D0%92%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%BD%D1%8B%D0%B5+%D1%82%D0%B5%D0%B3%D0%B8)).

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/f0e/d70/ad6/f0ed70ad62a3142ef7c7116a8143a5c5.png)

  
Для task вложенные теги определяют вид действия:  
\- task/now — выполнить сейчас;  
\- task/next — потом/отложить;  
\- task/waiting — поручено/контроль;  
\- task/someday — когда-нибудь/может быть.

  
Также в Obsidian потребуется установить и настроить три комьюнити-плагина: [obsidian-dataview](https://github.com/blacksmithgu/obsidian-dataview), [obsidian-checklist-plugin](https://github.com/delashum/obsidian-checklist-plugin) и [obsidian-reminder](https://github.com/uphy/obsidian-reminder). Необходимы для визуализации в интерфейсе приложения:

-   панель с активными проектами;
    
-   панель с активными задачами, сгруппированными по виду действия;
    
-   панель с событиями, требующими напоминания о времени.
    

По итогам всех настроек алгоритм работы в Obsidian будет выглядеть следующим образом:

-   Создать новую заметку.
    
-   Применить к заметке шаблон выбранного типа.
    
-   Заполнить заметку, установить связи с другими заметками.
    
-   Просматривать и управлять задачами/проектами на боковых панелях (плагины).
    
-   Получать напоминания о предстоящих событиях.
    

## Настройка конфигурации Obsidian

> Для тех, у кого нет времени или желания настраивать вручную, я подготовил хранилище Vault Obsidian и выложил на GitHab [obsidian\_gtd\_vault](https://github.com/pavel-mlgn/obsidian_gtd_vault). Vault настроен и заполнен первичными данными. Можно подключить хранилище, все примеры в статье приводятся на его основе.

Заходим в настройки Obsidian:

1.  Проверяем, что в разделе «Встроенные плагины» (Core plugins) подключены:
    
    -   [Панель тегов](https://publish.obsidian.md/help-ru/%D0%9F%D0%BB%D0%B0%D0%B3%D0%B8%D0%BD%D1%8B/%D0%9F%D0%B0%D0%BD%D0%B5%D0%BB%D1%8C+%D1%82%D0%B5%D0%B3%D0%BE%D0%B2) (Tags).
        
    -   [Шаблоны](https://publish.obsidian.md/help-ru/%D0%9F%D0%BB%D0%B0%D0%B3%D0%B8%D0%BD%D1%8B/%D0%A8%D0%B0%D0%B1%D0%BB%D0%BE%D0%BD%D1%8B) (Templates).
        
    -   [Избранное](https://publish.obsidian.md/help-ru/%D0%9F%D0%BB%D0%B0%D0%B3%D0%B8%D0%BD%D1%8B/%D0%98%D0%B7%D0%B1%D1%80%D0%B0%D0%BD%D0%BD%D0%BE%D0%B5) (Bookmarks).  
        
2.  В [Сторонних плагинах](https://publish.obsidian.md/help-ru/%D0%9F%D1%80%D0%BE%D0%B4%D0%B2%D0%B8%D0%BD%D1%83%D1%82%D0%BE%D0%B5+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5/%D0%A1%D1%82%D0%BE%D1%80%D0%BE%D0%BD%D0%BD%D0%B8%D0%B5+%D0%BF%D0%BB%D0%B0%D0%B3%D0%B8%D0%BD%D1%8B) (Community plugins) находим и устанавливаем плагины:
    
    -   Dataview ([obsidian-dataview](https://github.com/blacksmithgu/obsidian-dataview)).
        
    -   Checklist ([obsidian-checklist-plugin](https://github.com/delashum/obsidian-checklist-plugin)).
        
    -   Reminder ([obsidian-reminder](https://github.com/uphy/obsidian-reminder)).  
        
3.  В настройках плагина «Шаблоны» указываем путь к папке с шаблонами, например Templates.  
    
4.  В настройках плагина Checklist:
    
    -   В Tag Name устанавливаем два значения — task и project (каждое значение в отдельной строке).
        
    -   В Group By выбираем Tag.
        
    -   В Group Sort выбираем “A -> Z”.
        
    -   В Include Files указываем `!Templates/**`.  
        
5.  В пункте настроек «Файлы и ссылки» (File & Links):
    
    -   В списке «Место для вложенных файлов по умолчанию» (Default location for new attachments) выбираем значение «В папке, указанной ниже» (In subfolder under current folder).
        
    -   В текстовом поле «Путь к папке для вложенных файлов» (Subfolder name) указываем Attachments.  
        
6.  Завершаем настройки и возвращаемся в главное окно программы:
    
    -   На панели файлового менеджера (Files) создаем две корневые папки — Templates и Attachments (названия папок должны совпадать с заданными в настройках в п. 3 и 5).
        
    -   Компонуем боковые панели интерфейса по собственному вкусу. Ненужные удаляем.
        

В итоге должно получиться примерно так:

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/98c/8b8/bfe/98c8b8bfefca8e500e965d6276298941.png)

## Настройка шаблонов Obsidian

[Создадим пять шаблонов](https://publish.obsidian.md/help-ru/%D0%9F%D0%BB%D0%B0%D0%B3%D0%B8%D0%BD%D1%8B/%D0%A8%D0%B0%D0%B1%D0%BB%D0%BE%D0%BD%D1%8B) для каждого из типа заметок. Напомню, это:

-   **Inbox** — заметка для фиксации идей, мыслей, планов и т. п.
    
-   **Task** — задача, подразумевает единичное действие.
    
-   **Project** — проект, состоит из одного и более действий.
    
-   **Meeting** — встреча, собрание, то, что требует напоминания.
    
-   **Reference** — справочные материалы.
    

> Шаблоны — это обычные заметки, размещаются в директории Templates файлового менеджера.

В шаблонах будет, в частности, использоваться функциональность плагина Dataview. Плагин позволяет формировать представления на основе [запросов к заметкам](https://blacksmithgu.github.io/obsidian-dataview/queries/structure/) Obsidian. Общий формат запросов такой:

````
```dataview
  <QUERY-TYPE> <fields>
  FROM <source>
  <DATA-COMMAND> <expression>
  <DATA-COMMAND> <expression>
          ...
```
````

Сделаем так, чтобы в каждой нашей заметке мы сразу видели все ее обратные (backlinks) и исходящие (outgoing) ссылки. Для этого в шапку всех шаблонов добавляем следующий dataview-запрос:

````
```dataview
  TABLE without id
  file.outlinks AS "OUTGOING", 
  file.inlinks AS "BACKLINKS"
  WHERE file.name = this.file.name 
```
````

Очень удобно видеть всю информацию о ссылках непосредственно в документе. Также это сэкономит место в интерфейсе, так как панели для входящих/исходящих ссылок можно будет убрать.

Если кому-то важно видеть в заметке дату ее создания и последней модификации, то можно добавить еще такой запрос:

````
```dataview
  TABLE without id
  dateformat(this.file.ctime, "dd.MM.yyyy HH:mm") as created,
  dateformat(this.file.mtime, "dd.MM.yyyy HH:mm") as "last modified" 
  WHERE file.name = this.file.name
```
````

Далее определим шаблоны для каждого типа заметки, названия шаблонов будут совпадать с типами. Все шаблоны обязательно должны находиться в созданной нами директории Templates.

### Шаблон Task

````

```dataview 
TABLE without id
file.outlinks AS "OUTGOING", 
file.inlinks AS "BACKLINKS"
WHERE file.name = this.file.name 
```

#task/now %% now | next | waiting | someday %%
- [ ] {{title}}


# Links


# Description
````

> В тексте шаблона могут присутствовать комментарии (не отображаются в режиме просмотра документа). Комментарий начинается и заканчивается двойным символом процента: %%. В примере присутствует комментарий с перечислением всех возможных подтипов задачи.

Шаблон содержит:

-   Тег, обозначающий вид действия (по умолчанию всегда task/now — выполнить сейчас).
    
-   Чекбокс `- []` для фиксации статуса заявки: активная/завершена.
    
-   Переменная {{title}}. В момент применения шаблона подменяется на заголовок заметки.
    
-   Два раздела — Links (для размещения ссылок на внешние или внутренние ресурсы) и Descriptions (описание, текст заметки).
    

> Здесь и далее шаблоны имеют упрощенный вид, и их можно и нужно подстраивать под себя. Однако чекбоксы и теги должны оставаться в исходном виде.

### Шаблон Project

````
  
```dataview 
TABLE without id
file.outlinks AS "OUTGOING", 
file.inlinks AS "BACKLINKS"
WHERE file.name = this.file.name 
```

#project
- [ ] {{title}}

# Todo List
> [!todo] Active
> ```dataview
>  TASK
>  FROM [[]]
>  WHERE !completed
>  SORT file.ctime desc
> ```

> [!todo] Completed
> ```dataview
>   TASK
>   FROM [[]]
>   WHERE completed
>   SORT file.ctime desc
>   LIMIT 30
> ```

# Links


# Description
````

Шаблон проекта аналогичен предыдущему, обозначается тегом project. Дополнительно в нем присутствует раздел Todo List, в котором через Dataview отображается список активных (Active) и завершенных (Completed) задач, ссылающихся на проект.

### Шаблон Meeting

````

```dataview 
TABLE without id
file.outlinks AS "OUTGOING", 
file.inlinks AS "BACKLINKS"
WHERE file.name = this.file.name 
```

#meeting
- [ ]  {{title}} (@{{date}} {{time}})


# Links


# Attendees


# Agenda
%%  Write down the nain topic to discuss %%


# Notes
%%  Cover any key information disscused in the meeting %%
````

Шаблон для встреч, собраний обозначается тегом meeting. В конце строки с чекбоксом присутствует набор значений `(@{{date}} {{time}})`:

-   `{{date}} {{time}})` — переменные, автоматически подменяются текущей датой и временем в формате YYYY-MM-DD HH:MM.
    
-   `(@...)` — относится к функциональности плагина Reminder. Более подробно [смотрите документацию](https://obsidian-reminder.cf/guide/set-reminders.html#reminder-format). Внутри скобок указывается точная дата и время события, которое отображается на панели Reminders, и в назначенный час в интерфейсе Obsidian сработает напоминание.
    

### Шаблон Inbox и Reference

Последние два шаблона самые простые. Содержат только соответствующий тег inbox или reference и какие-то дополнительные разделы. Настраиваются по собственному усмотрению.

```

#inbox

# Description
```

````

```dataview 
TABLE without id
file.outlinks AS "OUTGOING", 
file.inlinks AS "BACKLINKS"
WHERE file.name = this.file.name 
```

#reference

# Links

# Description
````

## Как это все работает

А теперь разберемся, как будет выглядеть работа в Obsidian после всех настроек. Логика работы так или иначе должна соответствовать базовым принципам Get Things Done.

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/61d/c1e/9bd/61dc1e9bdc549a20b072cc8134b54c67.png)

### Inbox

Создаем заметку и [применяем к ней шаблон](https://publish.obsidian.md/help-ru/%D0%9F%D0%BB%D0%B0%D0%B3%D0%B8%D0%BD%D1%8B/%D0%A8%D0%B0%D0%B1%D0%BB%D0%BE%D0%BD%D1%8B#%D0%92%D1%81%D1%82%D0%B0%D0%B2%D0%B8%D1%82%D1%8C+%D1%88%D0%B0%D0%B1%D0%BB%D0%BE%D0%BD) Inbox, когда нужно зафиксировать какие-то мысли, идеи, дела, планы.

> Рекомендую в настройках Obsidian перейти в раздел «[Сочетание клавиш](https://publish.obsidian.md/help-ru/%D0%9A%D0%B0%D1%81%D1%82%D0%BE%D0%BC%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F/%D0%9F%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8C%D1%81%D0%BA%D0%B8%D0%B5+%D1%81%D0%BE%D1%87%D0%B5%D1%82%D0%B0%D0%BD%D0%B8%D1%8F+%D0%BA%D0%BB%D0%B0%D0%B2%D0%B8%D1%88)» (Hotkeys) и в пункте «Шаблоны: вставить шаблон» (Templates: Insert template) задать клавиши для быстрой вставки шаблона.

Данный шаг можно пропустить (сразу перейти к созданию Task, Project или др.), если есть полное понимание, что делать с данными, и есть время для их обработки прямо сейчас.

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/546/fcd/2de/546fcd2de076f1fdaa1afb29c61f0c9d.png)

Периодически обрабатываем накопленные в Inbox заметки. На их основе создаем новые заметки Task (задача), Project (проект), Reference (справочные материалы), Meeting (встреча). Неактуальные inbox-заметки удаляем.

Для контроля inbox-заметок можно создать пустую заметку Inbox Notes (добавить в «Избранное») и разместить в ней dataview-запрос, который отображает все существующие inbox-заметки:

````
```dataview
  LIST 
  FROM #inbox and -"Templates"
```
````

### Task

Для каждой задачи создаем заметку и применяем к ней шаблон Task. В зависимости от того, нужно ли приступить к выполнению сразу, потом или делегировать, меняем тег на task/now, task/next или task/wait соответственно. Если не требуется немедленных действий, но, может быть, когда-нибудь мы еще вернемся к этой работе, исправляем тег на task/someday.

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/804/16f/7ce/80416f7cea983f1fe9b990afbcd2dced.png)

### Project

Если предполагаются комплексные работы с необходимостью планирования, создаем заметку из шаблона Project.

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/32a/6dc/ce8/32a6dcce84b2940c16c19b59306c4163.png)

В рамках планирования для каждого шага проекта создаем отдельные задачи (шаблон Task). Для связи задач с проектом во всех задачах в разделе Links указываем [markdown-ссылку](https://publish.obsidian.md/help-ru/%D0%A0%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%B0/%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5+%D0%B2%D0%BD%D1%83%D1%82%D1%80%D0%B5%D0%BD%D0%BD%D0%B8%D1%85+%D1%81%D1%81%D1%8B%D0%BB%D0%BE%D0%BA#%D0%A1%D1%81%D1%8B%D0%BB%D0%BA%D0%B0+%D0%BD%D0%B0+%D0%B7%D0%B0%D0%BC%D0%B5%D1%82%D0%BA%D1%83) на проект `[[имя проекта]]`.

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/4b6/05e/781/4b605e781bbf6f473b8bb5bceb556754.png)

Если одну из задач отметить выполненной и вернуться на страницу проекта, то в разделах Active и Completed (Dataview) отобразятся все активные и завершенные задачи, связанные с проектом. В Backlinks увидим список заметок, ссылающихся на проект. В интерфейсе на боковой панели плагина Checklist (Todo List) отобразятся активные проекты и задачи, сгруппированные по виду действия.

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/23a/524/d40/23a524d40fd79cab49aebc277700eb3f.png)

### Meeting

Если планируется встреча или собрание, создаем заметку из шаблона Meeting.

> К сожалению, встроенной в Obsidian функциональности напоминаний не существует. Реализуется через комьюнити-плагины, например Reminder. В панели компонента отображается список запланированных событий, а в установленное время в интерфейсе появляется окно с напоминанием.
> 
> Дата и время события [прописывается в заметке](https://obsidian-reminder.cf/guide/set-reminders.html#reminder-format) в строке с чекбоксом в формате (`@YYYY-MM-DD HH:mm)`. Формат меняется в настройках плагина.

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/528/a74/a50/528a74a501c64410a6ee9c0891e632ea.png)

### Reference

Если данные являются справочной информацией, фиксируем их в заметке (шаблон Reference).

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/e8b/708/2e9/e8b7082e9179c1bdd6e035e852b31914.png)

Для большей гибкости и удобства в Reference лучше всего добавить подтипы. Тогда для каждого подтипа потребуется сделать отдельный шаблон. Например, шаблон Ref-Person — для фиксации информации по людям (тег reference/person), Ref-Instruction — для инструкций (reference/instruction), Ref-document — для документов (reference/document) и т. д.

Рассмотрим пример с Ref-Person (reference/person). Через шаблон создаются заметки, каждая из которых соотносится с конкретным человеком. Тогда появляется возможность линковать задачи, проекты, встречи с конкретными исполнителями, участниками. Это удобно: так, в заметке «человека» в обратных ссылках (Backlinks) будет присутствовать вся информация о делах, в которых он был когда-либо задействован.

> В качестве префикса в заголовке заметки Person лучше всего подставлять символ @ — это позволит быстро находить людей в списке.

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/b92/cab/a2b/b92caba2b8e6823fa900c5311a003aba.png)

В заметке персоны можно фиксировать любую дополнительную информацию о человеке в тексте или во [frontmatter](https://publish.obsidian.md/help-ru/%D0%9F%D1%80%D0%BE%D0%B4%D0%B2%D0%B8%D0%BD%D1%83%D1%82%D0%BE%D0%B5+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5/%D0%97%D0%B0%D0%B3%D0%BE%D0%BB%D0%BE%D0%B2%D0%BE%D0%BA+YAML) (также см. [Metadata](https://help.obsidian.md/Editing+and+formatting/Metadata)). Данные из всех frontmatter визуализируются через Dataview, например, так:

````
```dataview 
    TABLE
    phone,
    department,
    position_ 
    FROM 
     #reference/person and -"Templates" 
    SORT file.name   
```
````

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/092/d8b/9e5/092d8b9e5d8eb5d6895de72ed6f84881.png)

## Best practice

### Горячие клавиши

Рекомендую изучить и подстроить под себя [сочетания клавиш](https://publish.obsidian.md/help-ru/%D0%9A%D0%B0%D1%81%D1%82%D0%BE%D0%BC%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F/%D0%9F%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8C%D1%81%D0%BA%D0%B8%D0%B5+%D1%81%D0%BE%D1%87%D0%B5%D1%82%D0%B0%D0%BD%D0%B8%D1%8F+%D0%BA%D0%BB%D0%B0%D0%B2%D0%B8%D1%88) (Hotkeys) для работы в интерфейсе. Это значительно повысит удобство и скорость работы. Базовые сочетания, которые могут пригодиться (Windows):

-   `Ctrl + ,` — открыть настройки.
    
-   `Ctrl + N` — создать новую заметку.
    
-   Вставка шаблона в заметку — задать в настройках, придумать сочетание.
    
-   `Ctrl + Alt + <-` — вернуться.
    
-   `Ctrl + E` — переключиться между режимами редактирования и просмотра.
    
-   `Ctrl + O` — меню быстрого перехода, поиск по заголовкам заметок.
    
-   `Ctrl + Shift + F` — глобальный текстовый поиск по содержимому заметок.
    

### Избранное

В системе можно создавать заметки, не связанные с задачами, проектами или встречами. Чтобы они не потерялись, их следует [заносить в избранное](https://publish.obsidian.md/help-ru/%D0%9F%D0%BB%D0%B0%D0%B3%D0%B8%D0%BD%D1%8B/%D0%98%D0%B7%D0%B1%D1%80%D0%B0%D0%BD%D0%BD%D0%BE%D0%B5). Своего рода аналог закрепленных сообщений. Отображаются на панели Boolmarks. Например, это могут быть заметки, содержащие:

-   данные о важных ресурсах, веб-ссылки;
    
-   справочную информацию;
    
-   дашборды с динамическими отчетами, формируемыми через плагин Dataview.
    

Как пример дашборда, можно создать заметку с Dataview, полностью воспроизвести функциональность плагина Checklist (панель Todo List).

Todo List dataview

```

> [!note] Meetings
> ```dataview
> task
> from #meeting  and -"Templates"    
> where !completed
> sort file.ctime desc

> [!important] Projects
> ```dataview
> task
> from #project and -"Templates"    
> where !completed
> sort file.ctime desc

> [!todo] Tasks
>> [!todo] Now
>> ```dataview
>> task
>> from #task/now and -"Templates"  
>> where !completed
>> sort file.ctime desc
>> ```
>
>> [!todo] Next
>> ```dataview
>> task
>> from #task/next and -"Templates"  
>> where !completed
>>  sort file.ctime desc
>>  ```
>
>> [!todo] Waiting
>> ```dataview
>> task
>> from #task/waiting and -"Templates"  
>> where !completed
>> sort file.ctime desc
>> ```
>
>> [!todo] Someday
>> ```dataview
>> task
>> from #task/someday and -"Templates"  
>> where !completed
>> sort file.ctime desc

> [!done] Completed
> ```dataview
> task
> from #task 
> where completed
> sort file.ctime desc
> limit 10
> ```
```

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/e6c/fea/125/e6cfea12562874a9326b7a7b131721d3.png)

### Внедряемый контент

Obsidian позволяет через обычную вставку [внедрять контент](https://help.obsidian.md/Linking+notes+and+files/Embedding+files) из других файлов или даже веб-источников (через <iframe>). Это помогает сделать контент заметки более живым и понятным. [Поддерживаются различные форматы](https://help.obsidian.md/Advanced+topics/Accepted+file+formats).

Есть возможность рисовать схемы, диаграммы, которые также внедряются в текст заметки. Это можно делать через плагины:

-   Excalidraw ([obsidian-excalidraw-plugin](https://github.com/zsviczian/obsidian-excalidraw-plugin))
    
-   Diagrams ([drawio-obsidian](https://github.com/zapthedingbat/drawio-obsidian))
    
-   PlantUML ([obsidian-plantuml](https://github.com/joethei/obsidian-plantuml))
    
-   [Mermaid Diagrams](https://mermaid.js.org/) (встроенный плагин)
    

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/4a7/fc8/244/4a7fc8244f8f061ca298a8e8d2aaf0f5.png)

### Заметки в виде графа

В интерфейсе можно визуализировать заметки ([Graph view](https://help.obsidian.md/Plugins/Graph+view)) в виде неориентированного графа, где вершины — это заметки, а ребра — это связи (линки) между заметками. Как это использовать, исходя из текущего контекста, каждый решает сам. Однако какой-то смысл в этом есть. При накоплении большого количества данных наверняка получится увидеть интересные взаимосвязи между задачами, проектами, информацией.

> У Graph view много настроек отображения — в частности, можно задать цвет заметок (вершин графа) в зависимости от условий, например по тегам.

![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/19d/d02/565/19dd025654e3f159932c97a480a4e3c4.png)

## Заключение

Obsidian — это действительно очень интересный и разносторонний инструмент. Можно сказать, «комбайн» заметок, легко настраиваемый под разные цели. Этому очень способствует большой набор [комьюнити-плагинов](https://obsidian.md/plugins). Есть мобильное приложение. Правда, трудность освоения Obsidian чуть выше, чем других приложений, но, уверен, оно того стоит.

Предложенное в статье решение является основой для настройки под свои потребности и способы ведения дел. Существуют другие плагины, с которыми можно поэкспериментировать в контексте статьи и при необходимости подстроить под себя:

-   [Tq-obsidian](https://github.com/tgrosinger/tq-obsidian)
    
-   [obsidian-tasks](https://github.com/obsidian-tasks-group/obsidian-tasks)
    
-   [Obsidian TODO Plugin](https://github.com/larslockefeer/obsidian-plugin-todo)
    
-   [Kanban](https://github.com/mgmeyers/obsidian-kanban)
    
-   [Daily Notes](https://help.obsidian.md/Plugins/Daily+notes) (встроенный плагин), легко встраивается в концепцию управления задачами
    

Надеюсь, статья была полезна всем, кто интересуется темой, или даже новичкам.






