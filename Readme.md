# Инструкция по работе с Git

## Создание репозитория
Для создания репозитория используется команда *git init*. Для того, чтобы создать репозиторий, отройте в терминале пустую папку и в нём напишите *git init*

## Добавление файла к коммиту
Для добавления файла к новому коммиту используется команда *git add*. Для этого в терминале с папкой-репозиторием выполните команду *git add <название файла>*.

## Создание коммитов
Для того, чтобы выполнить коммит, используется команда *git commit*. Для этого в терминале с папкой-репозиторием напишите команду *git commit -m <сообщение к коммиту>*. Сообщения к коммитам писать ***ОБЯЗАТЕЛЬНО***. Все файлы коммит должны быть предворительно добавлены.

## Определение состояния
Команда *git status* показывает информацию о текущем состоянии папки-репозитория: актуальна ли информация в ней и состоянии папки.

## Как посмотреть все коммиты
Чтобы открыть журнал всех изменений, используется команда *git log*. В терменале появится список всех проведенных коммитов.

## Отслеживание изменений
Чтобы увидеть, какие есть изменения, и сравнить сохраненную и еще не сохраненную версии, ипользуется команда *git diff*.

## Возвращение файла к предыдущему состоянию
Гит позволяет вернуть выбранный файл к состоянию на момент определенного коммита. Для этого используется команда *checkout*. Чтобы сделать это, мы копируем идентификатор нужного нам коммита и пишем следующую команду:  *git checkout <идентификатор коммита>*. А чтобы вернуться к текущему состоянию (последнему коммиту) файла - пишем команду *git checkout master*.

## Просмотреть историю действий
Для того, чтобы просмотреть в терминале список всех команд, используется команда *history*

## Очистка поля терминала
Для того, чтобы очистить поле терминала (убрать уже не нужное нам), используется команда *clear*

# Ветвление
## Создание новой верки
Основная ветка в каждом репозитории называется ***master***. Чтобы создать еще одну ветку,используется команда *git branch <название ветки>*. На момент создания новая ветка становится копией ветки *master*.

## Переход с одной ветки на другую
Для того, чтобы вывести список всех веток файла, используется команда *git branch*. После ввода этой команды, в поле терминала появится список всех веток и та ветка, на которой мы находимся в данный момент будет закрашена зеленым цветом.