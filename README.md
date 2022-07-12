# Bring-It-On

1. Добавьте в проект файл .gitignore и настройте так чтобы скрыть файлы с расширением .db, .log и директории с названиями target или bin.
1.1. echo ".db
> .log
>
> /target
> /bin" > .gitignore

2. Создайте ветку feature и добавьте в неё два коммита
2.1. git checkout -b feature
2.2. git add .gitignore
2.3. git commit -m "added .gitignore file"
2.4. git commit --allow-empty -m "commit 2"

3. Смержите ветку feature в main
3.1. git checkout main
3.1. git merge feature

4. Вернитесь в feature и создайте файл arrows.txt cледующего содержания:
The ship glides gently on the waves
As day turns into night
Выполните коммит.
4.1. git checkout feature
4.2. touch arrows.txt
4.3. echo "The ship glides gently on the waves
> As day turns into night" > arrows.txt
4.4. git add arrows.txt
4.5. git commit -m "added arrows.txt file with two lines"

5. Перейдите в main. Создайте там файл arrows.txt и добавьте следующий текст:
One thousand burning arrows
Fill the starlit sky
Выполните коммит.
5.1. git checkout main
5.2. touch arrows.txt
5.3. echo "One thousand burning arrows
> Fill the starlit sky" > arrows.txt
5.4. git add arrows.txt
5.5. git commit -m "added arrows.txt file with two lines"

6. Смержите feature в main решив конфликт: сохраните все 4 строки в файле arrows.txt в порядке их добавления в пунктах 4 и 5.
6.1. git merge feature
6.2. vim arrows.txt
6.3. git add arrows.txt
6.4. git commit
