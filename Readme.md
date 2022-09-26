# Инструкция по работе с Git

## Создание репозитория
Для создания репозитория используется команда *git init*. Для того, чтобы создать репозиторий, отройте в терминале пустую папку и в нём напишите *git init*

## Добавление файла к коммиту
Для добавления файла к новому коммиту используется команда *git add*. Для этого в терминале с папкой-репозиторием выполните команду *git add <название файла>*.

# Создание коммитов
Для того, чтобы выполнить коммит, используется команда *git commit*. Для этого в терминале с папкой-репозиторием напишите команду *git commit -m <сообщение к коммиту>*. Сообщения к коммитам писать ***ОБЯЗАТЕЛЬНО***. Все файлы коммит должны быть предворительно добавлены


## Создание репозитория
Для создания репозитория используется команда *git init*. Для того, чтобы создать репозиторий необходимо на диске создать папку, далее в программе VSCode зайти *Файл* -> *открыть папку* и выбрать в открывшемся проводнике созданную ранее папку.

## Добавление файла к коммиту
Для добавления нового файла к коммиту используется команда *git add*.

Для отслеживания файла и осуществления контроля версионности над этим файлом и программа Git их контролировала, необходимо добавить эти файлы как лтслеживаемые.Это делается с помощью команды *Add* внутри команды Git. Для этого подается команда "git add (название файла)". Разделителями в данной команде являются пробелы. Сам файл указывается с учетом регистра и расширением файла.

## Фиксация состояния файла (сохранение)

Для фиксации состояния файла мы обращаемся в терминале к программе Git ипередаем команду *"Git commit -m "Текст сообщения"*. В сообщении кратко указывается суть сделанных изменений в файле. Это делается для того, что бы далее открыв список сохранений мы могли понять, какие изменения были зафиксированы в том или ином сохранении.

## Просмотр различий в файлах. 

Когда у нас есть несколько зафиксированных состояний, мы можем между ними переключаться, и, более того, мы можем посмотреть разницу между текущим состоянием файла и зафиксированным сосотоянием файла.Эта операция делается с использованием команды *" git diff"*. Эта команда выведет информацию об удаленных и добавленых строках, наглядно увидев изменения в файле.

## Вывод всех коммитов, которые были сделаны.

Для вывода всех сохраненных комитов в данной ветке, используется команда *"Git log"*. Разделителем снова является пробел. При этом выводяься: хэш-код - набор букв и цифр, понятные Git, дата и время коммита, краткое описание.

## Переход между разными коммитами

Для перехода между разными коммитами используется команда *"Git checkout (набор символов - номер коммита)"*. При этом будет осуществлен переход в тот коммит (состояние файла), который был указан в команде.

## Работа с ветками

Для вывода всех имеющихся веток используется команда *"Git branch"*. при этом выведется список со всеми ветками и знаком (*) будет отмечена ветка, на которой мы располагаемся в настоящий момент (текущая ветка).

Для создания новой ветки необходимо обратиться к GIT с коммандой *"git branch (имя новой ветки)"*. Разделитклями снова являются пробелы.

ля удаления ненужной ветки необходимо подать команду *"Git branch -d (название удаляемой ветки). 

Для перехода между ветками используется команда *"Git checkout branch (название ветки, на котрую осуществляется переход) "*.

Для наглядного отображения дерева всех имеющихся коммитов в данной ветке используется команда "*Git log --graph"*.

Для сливания (объединения) двух веток используется команда *"Git merge (название ветки, которая должна быть добавлена к текущей)"*. Приэтом данная команда вызывается оттуда, куда необходимо добавить указанную в команде ветку.

## Удаленная работа с репозитрориями (на примере работы с ресурсом GITHUB)

### Копирование нового репозитория и перенос его на наш компьютер.

Заходим на сайт **Github.com** и регистрируемся на нем. Здесь через поиск можно найти разных авторов и разные проекты. Необходимо открыть готовый готовый репозиторий. Далее необходимо скачать файл и сделать его локальным репозиторием.Просмотрев предварительно имеющиеся файлы, нам необходимо нажать зеленую кнопку *"Code"*, и скопировать ссылку на данный репозиторий, нажав кнопку в виде двух квадратиков справа от ссылки. Далее в программе VSCode необходимо дать команду *"Git clone (скопированная ссылка с Github)"*. В результате появится копия репозитория на нашем компьютере и появится новая папка с названием репозитория на GITHUB.

Далее необходимо пеtместиться в необходимую папку. Для этого используется команда *"cd (название папки, на которую переходим)"*. 

### Отправка созданного репозитория на GITHUB.

Для начала традиционным способом создается папка, инициируется, далее в ней создается файл, добавляем его и делаем первый коммит. для заливки репозитория на GITHUB необходимо создать свой собственный аккаунт на GITHUB. 
Далее необходимо пошагово сделать следующие шаги:

1. При помощи команды *"Git remote add origin (ссылка на созданный на GITHUB репозиторий) связать локальный и удаленный репозитории 
2.  При помощи команды *"Git branch -M main"* указывается ветка, которая будет являться основной.
3. При помощи команды *"Git push -u origin main"* отправляем то, что есть на локальном репозитории в интернет.

При этом при первой попытке необходимо автоизоваться на GITHUB.

Далее при работе с файлом на локальном репозитории, делаем необходимые изменения, добавляем файл, делаем коммит и при помощи команды *"Git push"* отправляем эти изменения в интернет. 

Такая же схема используется и при обратной отправке изменений (выкачивание актуального состояния из удаленного репозитория).Для этого испоьзуется команда *"Git pull"*. При этом команда "pull" это сотавная команда. Она не только подтянет изменения с GITHUB? но и произведет слияние состояний на GITHUB и локальном компьютере.

### Использование запросов на внесение изменений (Pull Request).

1. Сначала при помощи кнопки "FORK" делаем свою отдельную копию репозитория.
2. Делаем Git clone для нашей версии этого репозитория
3. Создаем ветку с предлагаемыми измениями
4. Производим все изменения (!) ТОЛЬКО в этой ветке
5. Отправляем эти изменеия на свой аккаунт
6. В окне на GITHUB появляется возможность отправить pull request.
