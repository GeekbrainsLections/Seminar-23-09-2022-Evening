# Инструкция по работе с Git

## Создание репозитория
Для создания репозитория используется команда *git init*. Для того, чтобы создать репозиторий, отройте в терминале пустую папку и в нём напишите *git init*

## Добавление файла к коммиту
Для добавления файла к новому коммиту используется команда *git add*. Для этого в терминале с папкой-репозиторием выполните команду *git add <название файла>*.

# Создание коммитов
Для того, чтобы выполнить коммит, используется команда *git commit*. Для этого в терминале с папкой-репозиторием напишите команду *git commit -m <сообщение к коммиту>*. Сообщения к коммитам писать ***ОБЯЗАТЕЛЬНО***. Все файлы коммит должны быть предворительно добавлены

Просмотреть коммиты можно при помощи команды *git log*. 

Посмотреть, что находиться в рабочей директории можно командой *git status*.

## Работа с ветками

Сделать новую ветку и переключиться на нее можно командой *git checkout –b <имя новой ветки>*.

Просто сделать ветку, не переключаясь на нее можно командой *git branch <имя ветки>*.
Переключиться на ветку команда *git checkout <имя ветки>*.

Удалить ненужную ветку: *git branch -d <название_ветки>*.

Важно понимать, что ветка берет свое начало не от ветки, а от последнего коммита который находиться в той ветке, в которой вы находились.
Что бы смержить одну ветку в другую нужно вначале переключиться на ту ветку, в которую вы хотите смержить: *git checkout <имя ветки>*.

Потом получить последние изменения сделанные в этой ветке выполнив *git pull*.
Затем выполнить команду *git merge <имя ветки>*.

Команда *git branch -M main* означает, что главной веткой будет ветка main.

Обратите внимание на то, что перед тем как заводить новую ветку нужно выполнить git pull. Делается это по нескольким причинам.
+ Другой программист мог изменить код, в том числе внести такие изменения, которые повлияют на решение задачи, для которой вы заводите новую ветку. Эти изменения могут вам пригодиться при решении своей задачи.
+ Из-за этих изменений вы можете получить конфликт при мерже.
+ Больше шанс что у вас получится merge commit. Это не так плохо, как два предыдущих пункта. Но если можно избежать лишнего коммита, то почему бы этого не сделать?


Так выглядит работа с ветками в общих чертах.



## Работа с удаленным репозиторием
Если вы хотите присоединиться к разработке уже имеющегося проекта, то вам нужно будет скопировать этот репозиторий в свою локальную папку с удаленного репозитория. Делается это так:

git clone <url удаленного репозитория>

После чего в текущей папке появляется директория .git в которой и будет содержаться копия удаленного репозитория.

Когда коммитов накопиться достаточно много, чтобы ими можно было поделиться, вы выполняете команду *git push*. После чего ваши коммиты уходят в удаленный репозиторий.

Если нужно получить изменения из удаленного репозитория, то нужно выполнить команду *git pull*. После этого, в вашем локальном репозитории появятся те изменения, которые были отправлены другими программистами.

