# Инструкция по работе с Git

## Создание репозитория
Для создания репозитория используется команда *git init*. Для того, чтобы создать репозиторий, отройте в терминале пустую папку и в нём напишите *git init*

## Добавление файла к коммиту
Для добавления файла к новому коммиту используется команда *git add*. Для этого в терминале с папкой-репозиторием выполните команду *git add <название файла>*.

# Создание коммитов
Для того, чтобы выполнить коммит, используется команда *git commit*. Для этого в терминале с папкой-репозиторием напишите команду *git commit -m <сообщение к коммиту>*. Сообщения к коммитам писать ***ОБЯЗАТЕЛЬНО***. Все файлы коммит должны быть предворительно добавлены

## Добавление удалённого репозитория
Добавить удалённый репозиторий можно параметром *remote add*, указав *shortname и url* требуемого репозитория.

    git remote add awesomeapp https://github.com/someurl..

## Просмотр удалённых URL-адресов
Просматривать удалённые URL-адреса можно параметром *remote* с флагом *-v*. Этот параметр отображает удалённые подключения к другим репозиториям.

    git remote -v

Такая команда открывает доступ к интерфейсу управления удалёнными записями, которые хранятся в файле **.git/config** репозитория.

## Получение дополнительных сведений об удалённом репозитории
Получить подробные сведения об удалённом репозитории можно с помощью параметра *remote show* с указанием имени репозитория — например, origin.

    git remote show origin

Эта команда отображает список веток, связанных с удалённым репозиторием, а также рабочих станций, подключённых для получения и отправки файлов.

## Отправка изменений в удалённый репозиторий
Отправлять изменения в удалённый репозиторий можно параметром push с указанием имени репозитория и ветки.

    git push origin main

Эта команда передаёт локальные изменения в центральный репозиторий, где с ними могут ознакомиться другие участники проекта.

## Получение изменений из удалённого репозитория

Для загрузки изменений из удалённого репозитория используется параметр *pull*. Он скачивает копию текущей ветки с указанного удалённого репозитория и объединяет её с локальной копией.

    git pull

Также можно просмотреть подробные сведения о загруженных файлах с помощью флага *--verbose*.

    git pull --verbose

## Слияние удалённого репозитория с локальным
Слияние удалённого репозитория с локальным выполняется параметром *merge* с указанием имени удалённого репозитория.

    git merge origin

## Отправка новой ветки в удалённый репозиторий
Передать новую ветку в удалённый репозиторий можно параметром *push* с флагом *-u*, указав имя репозитория и имя ветки.

    git push -u origin new_branch

# Удаление удалённой ветки
Чтобы избавиться от удалённой ветки, используйте параметр push с флагом *--delete*, указав имя удалённого репозитория и имя ветки.

    git push --delete origin existing_branch

## Использование перебазирования
Для доступа к этой функции используйте параметр *rebase* с указанием имени ветки. Перебазирование — это процесс объединения или перемещения последовательности коммитов на новый родительский снимок.

    git rebase branch_name

Эта команда изменит основу ветки с одного коммита на другой, как если бы вы начали ветку с другого коммита. В Git это достигается за счёт создания новых коммитов и применения их к указанному базовому коммиту. Необходимо понимать, что, хотя ветка и выглядит такой же, она состоит из совершенно новых коммитов.

## Команды в Github
Разница между **fork** и **clone** в GitHub.

**fork** - Когда нам нравится чей-то репозиторий и мы хотели бы иметь его в собственном аккаунте на GitHub, мы делаем форк («вилку») этого репозитория, чтобы иметь возможность работать с ним отдельно.

Когда мы делаем форк репозитория, мы получаем экземпляр всего репозитория, со всей его историей. После *fork* мы можем делать с ним все, что угодно: оригинальная версия при этом не будет задета.

**clone** - это не то же самое, что и *fork*. Клон удаленного репозитория располагается локально. Фактически при клонировании копируются все данные, включая историю коммитов и существующие ветки.

## Что такое Pull request.
**Pull request** – этот попытка добавить собственные изменения в репозиторий другого владельца. Чтобы сделать такой запрос, нужно взять чей-то проект, создать отдельную ветку, а затем предложить слить ее с остальными.
