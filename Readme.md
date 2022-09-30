# Инструкция по работе с Git

## Создание репозитория
Для создания репозитория используется команда *git init*. Для того, чтобы создать репозиторий, отройте в терминале пустую папку и в нём напишите *git init*

## Добавление файла к коммиту
Для добавления файла к новому коммиту используется команда *git add*. Для этого в терминале с папкой-репозиторием выполните команду *git add <название файла>*.

## Создание коммитов
Для того, чтобы выполнить коммит, используется команда *git commit*. Для этого в терминале с папкой-репозиторием напишите команду *git commit -m <сообщение к коммиту>*. Сообщения к коммитам писать ***ОБЯЗАТЕЛЬНО***. Все файлы коммит должны быть предварительно добавлены

## Просмотр веток 
Для того, чтобы открыть список всех существующих веток, используется команда *git branch*, ввести ее необходимо в терминале папки-репозитория. 

## Создание новых веток 
Для того, чтобы создать новую ветку, используется команда *git branch*. Для этого в терминале напишите команду *git branch "название новой ветки"*.

Чтобы создать новую ветку и сразу же на нее перейти, используется команда *git checkout -b "название новой ветки"*.

## Переход на другую ветку 
Для того, чтобы перейти на другую, уже существующую ветку, используется команда *git checkout*. Для этого необходимо в терминале папки-репозитория ввести *git checkout "название ветки"*. 

## Удаление ветки 
Для того, чтобы удалить существующую ветку, используется команда *git branch -d*. Для этого, в терминале папки-репозитория необходимо написать *git branch -d "название ветки"*.

## Слияние веток 
Для того, чтобы слить ветки (добавить информцию в текущую ветку из какой-либо другой) используется команда *git merge*. Для этого, в терминале папки-репозитория необходимо ввести *git merge "название ветки"*.

## Конфликт при слиянии веток

Нередко, при слияния веток, в git происходит конфликт. Такая проблема появляется в результате несовпадения текста в текущей и сливаемой ветках. 

В git предусмотрено 4 варианта решения конфликта:

* "Accept Current Change" - принять текущую версию.
* "Accept Incoming Change" - принять ту версию, которая к нам пришла. 
* "Accept Both Changes" - оставить оба варианта.
* "Compare Changes" - сравнить варианты. 

## Внесение данных имени пользователя и электронной почты. 
В git обязательным условием является указание автора репозитория и его контактов. Это сделано исходя из принципа командной работы в git, чтобы не запутаться в том, какой автор какую работу выполнял. 

Перед первым началом работы, необходимо выполнить следующие команды: 
* git config --global user.name "Ваше имя"
* git config --global user.email "ваш адрес эл. почты"