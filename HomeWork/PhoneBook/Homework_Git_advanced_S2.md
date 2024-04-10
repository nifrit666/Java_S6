# ***Урок 4. Семинар: Работа с изменениями***

## Задание №1 
-	Склонируйте репозиторий https://github.com/sortedmap/git-advanced-s2

-	Создайте пустой удалённый репозиторий seminar-2


-	Удалите связь с текущим репозиторием: git remote remove origin

-	Подключите свой локальный репозиторий к новому удалённому:git remote add origin path


-	Отправьте изменения в новый удалённый репозиторий:
git push -u origin master

-	Просмотрите историю коммитов в репозитории при помощи git log

-	Просмотрите изменения в нескольких коммитах: git diff from to

### Решение ###

$ git clone https://github.com/sortedmap/git-advanced-s2

$ git remote –v

$ git remote remove origin

$ git remote add origin https://github.com/nifrit666/seminar-2.git


## Задание №2 ##
-	Найдите коммит, в котором в файле index.html был добавлен фрагмент class="fw-lighter" в строку 34 (используйте команду git blame)
-	Перейдите в отдельную ветку (имя ветки придумайте самостоятельно)
-	Отмените изменения, выполненные именно в данном коммите. Для этого используйте команду git revert commit
-	Опишите суть изменений в сообщении коммита (в открывшемся редакторе vim)
-	Просмотрите получившийся коммит и изменения в нём
- Отправьте этот коммит в свой репозиторий


### Решение ###
$ git blame index.html

(d014a17c (Daniil Pilipenko 2022-11-01 09:20:36 +0300 34)     <p class="fw-lighter">Введите текст в поле ниже, и система измерит и покажет его длину.</p>)

$ git log 
(commit d014a17ca049ad5389484b1cf29e695ab7d36dcf

Author: Daniil Pilipenko <sortedmap@gmail.com>

Date:   Tue Nov 1 09:20:36 2022 +0300)

$ git checkout -b 777-issue

$ git revert d014a17ca049ad5389484b1cf29e695ab7d36dcf

$ git log

(commit b25c31323d626977bfd5143cc411ff6d621956ad (HEAD -> 777-issue)

Author: «Andrey_Istomin» <an.istomin@gmail.com>

Date:   Wed Apr 10 00:32:42 2024 +0500

    Revert "text styles changed"
    This reverts commit d014a17ca049ad5389484b1cf29e695ab7d36dcf.)

$ git push -u origin 777-issue

