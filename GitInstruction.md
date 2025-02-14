
# Инструкция по работе с git

## Что это и для чего нужна система контроля версий?

Программное обеспечение контроля версий отслеживает все вносимые в код изменения в специальной базе данных. При обнаружении ошибки разработчики могут вернуться назад и выполнить сравнение с более ранними версиями кода для исправления ошибок, сводя к минимуму проблемы для всех участников команды.

### Что такое система контроля версий?

### Для чего нужна система контроля версий

## Установка git и VSCode на ваш ПК.

### Установка VSCode на ваш ПК.

### Скачивание

Скачать дистрибутив вы можете на сайте проекта - https://code.visualstudio.com/

Объем дистрибутива около 70 мегабайт.

После скачивания запускаем установку.

### Установка

Саму установку нет смысла подробно описывать, единственное что вы можете поставить галочку напротив «Создать значок на рабочем столе», а так всё сводится к нажатию на кнопку «Далее» и в конце «Установить».

### Первый запуск

После установки среда запуститься автоматически.

### Установка git на ваш ПК
Включаем комп, открываем инструкцию
#### Первая настройка git

## Создание и базовая работа с локальным репозиторием.

Для создания локального репозитория необходимо инициализировать локальный репозиторий командой *git init*

далее нужно необходимо добавить файлы в отслеживаемые командой *git add*

для создания коммитов(сохраниний) используется команда *git commit -m "коментарий к коминту"*

### Что такое репозиторий и инструкция по созданию локальных репозиториев.
Обычно вы получаете репозиторий Git одним из двух способов:

Вы можете взять локальный каталог, который в настоящее время не находится под версионным контролем, и превратить его в репозиторий Git, либо

Вы можете клонировать существующий репозиторий Git из любого места.

В обоих случаях вы получите готовый к работе Git репозиторий на вашем компьютере.

Создание репозитория в существующем каталоге
Если у вас уже есть проект в каталоге, который не находится под версионным контролем Git, то для начала нужно перейти в него. Если вы не делали этого раньше, то для разных операционных систем это выглядит по-разному:

для Linux:

$ cd /home/user/my_project
для macOS:

$ cd /Users/user/my_project
для Windows:

$ cd C:/Users/user/my_project
а затем выполните команду:

$ git init
Эта команда создаёт в текущем каталоге новый подкаталог с именем .git, содержащий все необходимые файлы репозитория — структуру Git репозитория. На этом этапе ваш проект ещё не находится под версионным контролем. Подробное описание файлов, содержащихся в только что созданном вами каталоге .git, приведено в главе Git изнутри

Если вы хотите добавить под версионный контроль существующие файлы (в отличие от пустого каталога), вам стоит добавить их в индекс и осуществить первый коммит изменений. Добиться этого вы сможете запустив команду git add несколько раз, указав индексируемые файлы, а затем выполнив git commit:

$ git add *.c
$ git add LICENSE
$ git commit -m 'Initial project version'
Мы разберем, что делают эти команды чуть позже. Теперь у вас есть Git-репозиторий с отслеживаемыми файлами и начальным коммитом.

Клонирование существующего репозитория
Для получения копии существующего Git-репозитория, например, проекта, в который вы хотите внести свой вклад, необходимо использовать команду git clone. Если вы знакомы с другими системами контроля версий, такими как Subversion, то заметите, что команда называется «clone», а не «checkout». Это важное различие — вместо того, чтобы просто получить рабочую копию, Git получает копию практически всех данных, которые есть на сервере. При выполнении git clone с сервера забирается (pulled) каждая версия каждого файла из истории проекта. Фактически, если серверный диск выйдет из строя, вы можете использовать любой из клонов на любом из клиентов, для того, чтобы вернуть сервер в то состояние, в котором он находился в момент клонирования (вы можете потерять часть серверных хуков (server-side hooks) и т. п., но все данные, помещённые под версионный контроль, будут сохранены, подробнее об этом смотрите в разделе Установка Git на сервер главы 4).

Клонирование репозитория осуществляется командой git clone <url>. Например, если вы хотите клонировать библиотеку libgit2, вы можете сделать это следующим образом:

$ git clone https://github.com/libgit2/libgit2
Эта команда создаёт каталог libgit2, инициализирует в нём подкаталог .git, скачивает все данные для этого репозитория и извлекает рабочую копию последней версии. Если вы перейдёте в только что созданный каталог libgit2, то увидите в нём файлы проекта, готовые для работы или использования. Для того, чтобы клонировать репозиторий в каталог с именем, отличающимся от libgit2, необходимо указать желаемое имя, как параметр командной строки:

$ git clone https://github.com/libgit2/libgit2 mylibgit
Эта команда делает всё то же самое, что и предыдущая, только результирующий каталог будет назван mylibgit.

### Базовая работа с локальным репозиторием

## Ветки. Локальная работа с ветками в git.

### Что такое ветки и для чего они нужны при работе с системой контроля версий.

### Базовая работа с ветками в git.

## Работа с удаленными репозиториями.

### Что такое удаленный репозиторий и для чего он нужен
    > Удалённые репозитории — это модификации проекта, которые хранятся на удалённом сервисе (github, gitlab).
    > Необходим для общей командной работы.

### Базовая работа с удаленными репозиториями GitHub

## Совместная работа над проектом (fork, pull request)

### Инструкция по созданию pull request

1. Делаем форк (fork) интересующщего нас репозитория.
2. Делаем git clone для нашей версии этого репозитория.
3. Мы создаем ветку с предлагаемыми изменениями.
4. Производим все изменения только в этой ветке.
5. Отправляем все эти изменения на свой аккаунт (push).
6. В окне Github появляется возмжность отправить pull request.

### Как строится и для чего нужна совместная работа в системах контроля версий


