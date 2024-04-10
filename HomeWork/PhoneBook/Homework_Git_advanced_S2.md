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

