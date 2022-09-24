# Инструкция по работе с Git

## Создание репозитория
Для создания репозитория используется команда *git init*. Для того, чтобы создать репозиторий, отройте в терминале пустую папку и в нём напишите *git init*

## Добавление файла к коммиту
Для добавления файла к новому коммиту используется команда *git add*. Для этого в терминале с папкой-репозиторием выполните команду *git add <название файла>*.

# Создание коммитов
Для того, чтобы выполнить коммит, используется команда *git commit*. Для этого в терминале с папкой-репозиторием напишите команду *git commit -m <сообщение к коммиту>*. Сообщения к коммитам писать ***ОБЯЗАТЕЛЬНО***. Все файлы коммит должны быть предворительно добавлены

## В каком состоянии находится файл

Для того, чтобы определить состояние файла/папки необходимо ввести команду "git status".

## Просмотр имеющихся коммитов

Для того, чтобы посмотреть созданнные коммиты или вернуться к сохраненному коммиту, необходимо ввести команду "git log".

## Слияние веток

Когда, в дополнительно ветке создан и отредоктирован файл до нужного состояния, необходимо "слить" эту ветку с исходной веткой - master.
Для этого необходимо ввести команду "git merge namebranch".

## Информация по работе с ветками

Для создания новой ветки и работы в ней есть несколько возможных команд:
1. Команда "git branch" - создание новое ветки;
2. Команда "git checkout namebranch" - переход на новую ветку;
3. Команда "git checkout -b namebranch" - создание и переход на новую ветку;
4. Команда "git branch -d namebranch" - удаление ненужной ветки.

## Работа с репозиторием на GITHUB

Для работы в удаленном репозитории, необходимо с сайта ![github.com](https://github.com):
1. Во вкладке "CODE" скопировать html код.
2. В терминале ввести команду "git clone" и вставить скопированный html код
3. Команда "CD" - позволяет перейти в папку git или правой кнопкой мыши щелкнув на папку выбрать "Открыть во встроенном терминале"
4. Для подключения удаленного репозитория нужна команда "git remote add origin master"
5. Комнада "git log --graph" - позволяет посмотреть все созданные коммиты (какая происходит работа в данный момент)
6. Комнада "git push -u" - передача файлов в репозиторий
7. Комнада "git pull" - вытащить/притянуть файлы из репозитория
