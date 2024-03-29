# Инструкция по работе с ***Git***

## Что такое ***Git***?

Git (Global Information Tracker) - проект был создан Линусом Торвальдсом для управления разработкой ядра Linux, первая версия выпущена 7 апреля 2005 года.

![Linus Torvalds](Linus_Torvalds.jpg)

Торвальдс так саркастически отозвался о выбранном им названии git (что на английском сленге означает «мерзавец»):

>Я эгоистичный ублюдок, и поэтому называю все свои проекты в честь себя. Сначала Linux, теперь git.

```sh
Git - это распределенная система управления версиями. Это означает, что локальный клон проекта является полным репозиторием управления версиями. Полнофункциональные локальные репозитории упрощают работу в автономном режиме или в удаленном расположении. Разработчики фиксируют свою работу локально, а затем синхронизируют свою копию репозитория с копией на сервере.
```
Узнать больше информации про Git можно на сайте [Википедии](https://ru.wikipedia.org/wiki/Git)

### Выделение текста в Markdown

Чтобы выделить текст курсивом необходимо обрамить его "*" или "_" вот так ```*текст* или _текст_```, a чтоб выделить полужирным используй следующие комбинации - ```**текст** или __текст__```
При желании их также можно комбинировать.

### Подготовка репозитория

Команда *git init* создает новый репозиторий *Git*. С ее помощью можно преобразовать существующий проект без управления версиями в репозиторий *Git* или инициализировать новый пустой репозиторий. Большинство остальных команд *Git* невозможно использовать без инициализации репозитория, поэтому данная команда обычно выполняется первой в рамках нового проекта.

### Создание точек фиксации. Команда ***"git add"***

Команда *git add :/* добавляет в индекс все файлы независимо от того, в какой директории вы находитесь.

### Добавление комментариев к точекам фиксации. Команда ***"git commit"***

Команда *git commit -m "Комментарий к коммиту"* - фиксирует изменения. До выполнения этой команды локальные изменения никуда не запишутся.

Нужно правильно разбивать изменения и давать полные комментарии к коммитам.

### Команда ***"git log"***

Выводит список всех коммитов. С помощью *git log* можно посмотреть историю коммитов.

### Команда ***"git log --oneline и --graph"*** 

У команды *git log* есть разные опции, самая используемая из них - *--oneline*. Она показывает хеш в укороченном формате, ветку, в которой сделан коммит, а также текст коммита. Чтобы использовать эту опцию (как и любую другую), нужно добавить её после команды: *git log --oneline*. Опция oneline является особенно полезной с опцией *--graph* команды log. С этой опцией вы сможете увидеть небольшой граф в формате ASCII, который показывает текущую ветку и историю слияний:

```sh
git log --oneline --graph
```

### Команда ***"git checkout"***

В *Git* под термином *checkout* подразумевают переключение между различными версиями целевого объекта. Команда *git checkout* работает с тремя различными объектами: файлами, коммитами и ветками. Под переключением также обычно понимают действие, связанное с выполнением команды *"git checkout"*.

### Команда **_"git_branch"_**

Это команда для управления ветками в репозитории Git.

```sh
git branch -d<branch_name>
```

Удаление указанной ветки. Это «безопасная» операция, поскольку Git не позволит удалить ветку, если в ней есть неслитые изменения. 

```sh
git branch -D<branch_name>
```
 Принудительное удаление указанной ветки, даже если в ней есть неслитые изменения. Эта команда используется, если вы хотите навсегда удалить все коммиты, связанные с определенным направлением разработки.

### Добавление изображений в Markdown

Это может показаться неочевидным, но вы можете добавлять изображения в Markdown.

Все, что вам нужно сделать, это использовать синтаксис Markdown, подобный этому:

```sh
![git image](git.jpeg)
```

Альтернативный текст - это, по сути, способ описания изображения. Он не отображается в отображаемом тексте. Вы даже можете не указывать его, если хотите:

Вот пример

![git image](git.jpeg)

## Работа с удаленными репозиториями. Сервис GitHub.

