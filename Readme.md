# Инструкция по работе с Git

## Создание репозитория
Для создания репозитория используется команда *git init*. Для того, чтобы создать репозиторий, отройте в терминале пустую папку и в нём напишите *git init*

## Добавление файла к коммиту
Для добавления файла к новому коммиту используется команда *git add*. Для этого в терминале с папкой-репозиторием выполните команду *git add <название файла>*.

## Создание коммитов
Для того, чтобы выполнить коммит, используется команда *git commit*. Для этого в терминале с папкой-репозиторием напишите команду *git commit -m <сообщение к коммиту>*. Сообщения к коммитам писать ***ОБЯЗАТЕЛЬНО***. Все файлы коммит должны быть предворительно добавлены

## Определение состояния
Для того, чтобы получить информацию о текущем состоянии репозитория: актуальна ли информация на нём, нет ли чего-то нового, что поменялось, и так далее. Для этого в терминале необходимо ввести команда  *git status*.

## Отслеживание коммитов
Для просмотра все выполненных фиксаций можно воспользоваться историей коммитов. Она содержит сведения о каждом проведенном коммите проекта. Запросить ее можно при помощи команды *git log* В ней содержиться вся информация о каждом отдельном коммите, с указанием его хэша, автора, списка изменений и даты, когда они были сделаны. Отследить интересующие вас операции в списке изменений, можно по хэшу коммита, при помощи команды 

     *git show hash_commit*.

 ## Изменение комментария коммита
Если есть необходимость переделать commit message и внести туда новый комментарий, можно написать следующую конструкцию:

    *git commit --amend -m 'Новый комментарий'*. 
В данном случае сообщение последнего коммита перезапишется. Но злоупотреблять этим не стоит, поскольку эта операция опасная и лучше ее делать до отправки коммита на сервер.

## Просмотр изменений 
Для вывода изменений в файлах по сравнению с последним коммитом, используется *git diff*.
Команда выводит изменения в файлах, которые еще не были добавлены в индекс. Сравнение происходит с последним коммитом.

### Сравнение с последним коммитом, включая файлы в индексе
Если вы изменили какие-нибудь файлы в вашем рабочем каталоге и добавили один или несколько из них в индекс (с помощью *git add*), то команда *git diff* не покажет изменения в этих файлах. Чтобы показать изменения в файлах, включая файлы, добавленные в индекс, используется ключ *--cached*: 
*git diff --cached*.

### Сравнение коммитов
Команда *git diff* позволяет сравнивать два различных коммита. Сначала нужно определить хеш (ID) коммитов, которые требуется сравнивать. Можно воспользоваться командой *git log*, чтобы вывести список коммитов и их идентификаторы:

*git log --oneline*

Теперь сравним два коммита. Для этого в качестве первого аргумента команде *git diff* указывается хеш первого коммита, а вторым аргументом хеш второго коммита, например:

*git diff 4612297 5e356cf*.

## Создание новой ветки

Основная ветка в каждом репозитории называется *master*. Чтобы создать еще одну ветку, используем команду *branch* <name>.

Например:  
*git branch amazing_new_feature*. 
Это создаст новую ветку, пока что точную копию ветки master.

## Переключение между ветками

В Git ветка — это отдельная линия разработки. *Git checkout* позволяет нам переключаться как между удаленными, так и меду локальными ветками. Это один из способов получить доступ к работе коллеги или соавтора, обеспечивающий более высокую продуктивность совместной работы. Однако тут надо помнить, что пока вы не закомитили изменения, вы не сможете переключиться на другую ветку. В такой ситуации нужно либо сделать коммит, либо отложить его, при помощи команды *git stash*, добавляющей текущие незакоммиченные изменения в стек изменений и сбрасывающей рабочую копию до HEAD'а репозитория.

К примеру, если мы запустим *branch*, то увидим две доступные опции:
### git branch
    amazing_new_feature
    * master
master — это активная ветка, она помечена звездочкой. Но мы хотим работать с нашей “новой веткой”, так что нам понадобится переключиться на другую ветку. Для этого воспользуемся командой *checkout*, она принимает один параметр — имя ветки, на которую необходимо переключиться. 

Например:

    git checkout amazing_new_feature

## Слияние веток

Для слияния веток используется команда *merge* и переносит изменений с одной ветки на другую. При этом слияние не затрагивает сливаемую ветку, то есть она остается в том же состоянии, что позволяет нам потом продолжить работу с ней. 

Например: 

     Переключимся на основную ветку 
      #git checkout master
      Сольем изменения с ветки <сливаемая ветка> в ветку master
      #git merge <сливаемая ветка>
Теперь ветка *master* актуальна. Ветка <сливаемая ветка> больше не нужна, и ее можно удалить.

Например:

     git checkout master
     git merge lists
     git log
     git branch
     git branch -d lists
     git branch
             

Если хотите создать копию удаленного репозитория - используйте git clone. Однако если вам нужна только определенная его ветка, а не все хранилище - после git clone выполните следующую команду в соответствующем репозитории:

git checkout -b <имя ветки> origin/<имя ветки>
После этого, новая ветка создается на машине автоматически.


