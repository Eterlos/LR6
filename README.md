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

Чтобы выполнить слияние двух веток в ветку master, необходимо сначала переключиться на неё с помощью git checkout master. После команды git merge new_master происходит слияние. Слияние произошло без конфликтов по той причине, что ветки абсолютно идентичны:

![Screen11](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen11.png?raw=true)

С помощью создания нового файла merge_commitfile.txt и коммита было зафиксировано слияние:

![Screen12](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen12.png?raw=true)

Побочная ветка new_master была удалена с помощью команды git branch -d new_master. После этого был сразу создан файл del_commitfile.txt и сделан новый коммит, где было зафиксировано удаление этой ветки:

![Screen13](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen13.png?raw=true)

Были удалены ненужные файлы merge_commitfile.txt и del_commitfile.txt. Дополнительно в каталог были добавлены 2 изображения: myrecs_photo.png и musor.png. Для каждого были сделаны коммиты, а myrecs_photo.png было загружено в репозиторий. Коммит со вторым изображением был отменён с помощью команды git revert master. После применения команды открылся редактор, после закрытия которого в консоль вывелась информация, что коммит со вторым изображением действительно был удалён:

![Screen14](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen14.png?raw=true)

![Screen15](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen15.png?raw=true)

![Screen16](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen16.png?raw=true)

Также был добавлен ещё один текстовый файл book.txt:

![Screen17](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen17.png?raw=true)

Дополнительно добавился файл animals.txt. Он был загружен в репозиторий. После этого с помощью команды echo в файлы new_textfile.txt, book.txt и animal.txt была добавлена текстовая информация. С помощью git add изменённые файлы были загружены. Дальше был сделан коммит и данный «слепок» изменений был загружен в репозиторий:

![Screen18](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen18.png?raw=true)

Для отчёта была создана специальная ветка otchet:

![Screen19](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen19.png?raw=true)

В ветке otchet, а конкретнее в файле README.md будет храниться данный написанный отчёт. Используя язык разметки Markdown в Visual Studio Code можно начинать оформлять и форматировать текст:

![Screen20](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen20.png?raw=true)

По данному началу можно сделать коммит. Так как ветка, в которой происходит работа, не является основной, то нужно прописать команду git push --set-upstream origin otchet:

![Screen21](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen21.png?raw=true)

На странице репозитория в GitHub начинают появляться первые штрихи отчёта:

![Screen22](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen22.png?raw=true)

В каталоге была создана отдельная папка screens, в которую были добавлены все скрины по ходу работы. Был сделан коммит, а после этого папка была внесена в репозиторий:

![Screen23](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen23.png?raw=true)

С помощью команды git log --pretty=format:"%h -- %cd, %an : %s" производится получение истории операций в форматированном виде благодаря указанию следующих параметров: %h — сокращённый хэш, %cd — дата, %an — имя автора, %s — комментарий:

![Screen24](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen24.png?raw=true)

Один из последних шагов — получение всех логов команд без результатов их выполнения. Это можно сделать благодаря history | grep “git” — эта команда позволит выполнять поиск в истории команд по “git”. На рисунке  представлена только часть из полученных логов из-за их большого количества:

![Screen25](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen25.png?raw=true)

Теперь остаётся обобщить некоторые логи и записать их:
+ git config user.name
+ git config user.email
+ git clone
+ git add <название файла>
+ git commit -m
+ git push
+ git show <хэш>
+ git log
+ git log --numstat
+ git branch
+ git log -p
+ git branch <название ветки>
+ git checkout <название ветки>
+ git merge <название ветки>
+ git branch -D <название ветки>
+ git revert <название ветки>
+ git rm <название файла>
+ git push --set-upstream origin <название ветки>
+ git log --pretty=format:”%h -- %cd, %an : %s”

В репозиторий были добавлены новые скрины для отчёта, а также новая версия файла README.md:

![Screen26](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen26.png?raw=true)

Таким образом, на следующих рисунках представлена запись отчёта на языке разметки Markdown в Visual Studio Code:

![Screen27](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen27.png?raw=true)

![Screen28](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen28.png?raw=true)

![Screen29](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen29.png?raw=true)

![Screen30](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen30.png?raw=true)

![Screen31](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen31.png?raw=true)

![Screen32](https://github.com/Eterlos/LR6/blob/otchet/screens/Screen33.png?raw=true)

## Вывод
Изучены базовые возможности системы управления версиями, получен опыт работы с Git Api, получен опыт работы с локальным и удалённым репозиторием.