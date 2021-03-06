# Инструкция по работе с GIT

Git - программа для контроля версий.
В программировании проблемы совместной работы над проектами возникли ещё до появления облачных сервисов. Программа Git берёт на себя контроль версии проекта и позволяет переключаться между ними. 

Обратите внимание: Git хранит не файлы целиком, а отличия между ними. Это позволяет экономить память. 
Автор программы — Линус Торвальдс, создатель ОС Linux.

Прежде чем создавать репозиторий и инициализировать Git, проверим текущую установленную
версию пограммы. Для этого в терминале введём команду:

    git --version

## <u>Создание репозитория</u>

Чтобы создать (инициализировать) новый репозиторий в текущей папке нужно в терминале ввести команду:

    git init

## <u>Проверка состояния репозитория</u>

Для того, чтобы проверить текущее состояние GIT, есть 
ли изменения, которые нужно закоммитить (сохранить), вводим команду:

    git status


## <u>Добавление версионности</u>

Команда:

    git add <name>

Добавляет содержимое рабочего каталога. Эта команда дается после добавления файлов. Чтобы заполнить автоматически вводим несколько первых букв названия файла и нажимается "tab".

## <u>Фикcация изменений</u>

Команда:

    git commit

Зафиксировать или сохранить. По умолчанию git commit использует лишь этот индекс, так что вы можете использовать git add для сборки слепка вашего следующего коммита.

Команда git commit берёт все данные, добавленные в индекс с помощью git add, и сохраняет их слепок во внутренней базе данных, а затем сдвигает указатель текущей ветки на этот слепок.

## <u>Журнал изменений</u>

Команда:

    git log

Показывает внесенные в файл изменения начиная с последнего. 

**Чтобы вернуться в командную строку нужно нажать "Q".**

Чтобы вывести внеенные изменения коротко, в одну строку, используем команду:

    git log --oneline

Для переключения между версиями (изменениями) используем команду:

    git checkout

Для работы нужно указать не только интересующий вас коммит, но и вернуться в тот, где работаем, при помощи команды 

    git checkout master    

Команда: 

    git diff

Показывает разницу между текущим файлом и сохранённым. Перед переключением версии файла в Git используйте команду git log, чтобы увидеть количество сохранений.

## <u>Синтаксис языка Markdown</u>


**Жирный текст** — ** text ** без пробела

 *Курсивный текст* — * текст *

~~Зачеркнутый текст~~

 # Выделяют заголовки — # в начале строки


Нумерованные Списки 

1. обычными цифрами 1, 2, 3
2. 

 Ненумерованные Списки — обозначаются

* знаками в начале строки
*


**Вложенные Списки** 


 1. First item.
   - Item 1
   - Item 2
   - Item 3
1. Second item.
   - Nested item 1
      - Further nested item 1
      - Further nested item 2
      - Further nested item 3
   - Nested item 2
   - Nested item 3


## <u>Выделение текста</u>

Для выделения цитат используется знак больше ">".    

> Синтаксис Markdown не поддерживает подчеркивание текста. На вики-странице можно использовать HTML-тег "u" для создания подчеркнутого текста. Например, <u>underlined text </u> 

А если тег <Ю> оставить открытым, то весь внесесенный далее текст будет подчеркнутым до закрытия тега <>.

    Выделять текст так же можно с помощью - Tab.

## <u> Добавление изображений </u>

Чтобы добавить изображение, используйте следующий синтаксис:

![Text] (URL) - без пробела межsду квадратными и круглыми скобками.

![Пробуем добавлять картинки](https://images.wallpaperscraft.ru/image/single/plamia_voda_ruki_129994_1920x1080.jpg)


## <u>Работа с ветками в GIT</u>

Ветки в Git используются для совместной работы над проектом, а так же для разделения общей задачи на подзадачи. 

Кроме этого разделение на ветки в Git используются для работы с черновиками. 

* ### Просмотр всех веток

Для просмотра всех веток используется команда:

    git branch

Команда *git branch* показывает не только все ветки (черновики), которые есть в документе, но и *<u>саму ветку, на которой в данный момент находится пользователь.</u>* 

* ### Создание новой ветки

Для создания новой ветки используется команда:

    git branch <имя_ветки>
    

* ### Слияние веток

Для слияние веток используется команда:

    git merge

Чтобы совместить любую ветку с текущей необходимо набрать команду:

    git merge <имя_ветки>

При слиянии веток может возникнуть конфликт ~~интересов~~ изменений, когда в текущей папке в заданных строках уже находится какой-либо текст. 

В этом случае у нас есть несколько вариантов действий:

> Accept Current Change - принять текущие изменение.

> Accept Incoming Change - принять входящее изменение.

> Accept Both Changes - принять оба изменения.


* ### Удаление веток

После слияния веток и переноса текста (информации), ветку-черновик можно удалить. Для этого используется команда:

    git branch -d <имя_ветки>

    
* ### Визуализация веток

Для визуализации всех веток в удобном формате используется команда:

    git log --oneline --all --graph

   ## Работа с удаленными репозиториями
   
   
