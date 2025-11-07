# Лабораторная работа №6: Система контроля версий

## Цель работы
Изучение базовых возможностей системы управления версиями, получение опыта работы с Git Api, получение опыта работы с локальным и удалённым репозиторием.

## Ход работы
На сайте GitHub ранее уже был создан аккаунт, поэтому первый шаг — сделать форк репозитория из методических указаний к лабораторной работе:

![Screen1](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen1.png?raw=true)

Далее был настроен клиент git. С помощью команды git config --global user.name было указано имя пользователя, а с помощью команды git config --global user.email электронная почта:

![Screen2](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen2.png?raw=true)

С помощью команды cd был осуществлён переход в каталог на компьютере, где будет располагаться репозиторий. А с помощью команды git clone репозиторий и был склонирован на компьютер:

![Screen3](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen3.png?raw=true)

Был создан новый файл — new_testfile.txt. Этот файл был создан с помощью команды touch, добавлен с помощью команды git add. Теперь для того, чтобы изменения внеслись, нужно сделать коммит с помощью команды git commit -m. С помощью команды git push изменения были загружены в локальный репозиторий:

![Screen4](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen4.png?raw=true)

Теперь в локальном репозитории на GitHub можно увидеть созданный тестовый файл:

![Screen5](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen5.png?raw=true)

По заданию необходимо получить историю операций для каждой из веток. В начале нужно понять, сколько вообще веток в репозитории. Это можно сделать с помощью команды git branch. Так как ветка всего лишь одна (ветка master), то благодаря git log можно сразу получить историю её операций:

![Screen6](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen6.png?raw=true)

Далее с помощью команды git log -p в консоль выводится все изменения в каждом из коммитов репозитория:

![Screen7](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen7.png?raw=true)

Для выполнения последующих действий в репозитории необходимо создать новую ветку. Это будет ветка new_master. Новая ветка была создана благодаря команде git branch с указанием её имени, а потом благодаря этой же команде git branch была получена информация о ветках в репозитории:

![Screen8](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen8.png?raw=true)

Для новой ветки также необходимо получить историю её изменений. В начале с помощью команды git checkout нужно переключиться с изначальной ветки master в новую созданную ветку new_master. После же с применением уже ранее использованных команд git log и git log -p в консоль выведется информация обо всех изменениях в ветке, а также о её последних изменениях:

![Screen9](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen9.png?raw=true)

![Screen10](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen10.png?raw=true)