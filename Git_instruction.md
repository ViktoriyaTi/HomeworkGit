# Инструкция по работе с Git.

**Git** - программа, которая берет на себя вопросы контроля версий над проектом. 

Git  сохраняет в памяти не файлы целиком, а __разницу__ между файлами.

После установки программы - необходимо представиться, это необходимо сделать всего лишь один раз и git вас запомнит. 

Для этого в терминале необходимо ввести две команды:
+ git confing --global user.name "Ваше имя английскими буквами"
+ git confing --global user.email ваша_почта@mail.ru 

## Алгоритм действий:
1. Создать новую папку для работы.
2. Создать нужный файл (не забыть указать название файла с расширением).
3. Необходимо создать новый репозиторий(инициализировать), для этого необходимо ввести команду *git init*.
4. Необходимо добавить файл к отслеживанию с помощью команды *git add пробел название файл с расширением*. 

![git add](12345.png)

Для того чтобы постоянно не вносить полностью имена файлов поможет кнопка tab,которая дополнят название файла полностью, после внесения нескольких начальных символов имени файла.

5. С помощью команды *git status* можно просматривать текущий статус состояния.

После внесения изменений не забывать их сохранять - cntrl + s.

6. С помощью комманды *git commit -m "внести название коммита"* - сохранит изменения с комментарием.

7. С помощью команды *git log* - возможно просматривать журнал версий.

8. С помощью команды *git checkout название версии* - возможно перемещаться между версиями.
С помощью команды *git checkout master* - возможно вернуться в текущее состояние (а именно перейти на ветку master).
9. Команда *git diff* - показывает разницу между текущим файлом и тем состоянием,которое сохранено.

Шпаргалка по командам https://github.com/cyberspacedk/Git-commands

10. С помощью команды *git branch* - можно посмотреть на какой ветке мы работаем.
11. Команда _clear_ позволяет очистить всю информацию в терминале.
12. *Git branch название ветки* - позволяет добавить новую ветку.
13. Перемещаться между ветками - *git checkout название ветки* (например, git checkout master).

С помощью команды *git merge* - возможно слить одну ветку с текущуей.
Команда *git log --graph* - отображает список коммитов в виде графа (дерева).

## Работа с удаленным репозиторием

С помощью команды *git clone ссылка на адрес репозитория гитхаб* можно скопировать (склонировать) репозиторий,который находится на гитхабе.

Если мы хотим сами размещать репозиторий на гитхабе,то для этого необходимо:
* Перейти на github.
* Создать новый репозиторий (ввести название репозитория, определить его публичность и т.д).
* Скопировать ссылку на свой репозитрий.
* В терминале VS Code - *git remote add origin ссылка на наш репозиторий*, (первый раз необходимо связать git и github) затем git push origin master - направляем нашу версию репозитория на внешний репозиторий.
* Переходи на  github, обновляем страницу.
Команда git remote remove origin позволяет удалить origin.

Как сделать pull request?
1. делаем fork/
2. делаем git clone своей версии репозитория.
3. создаем новую ветку и в нее вносим свои изменения.
4. фиксируем изменения (коммиты).
5. отправляем свою версию в свой гитхаб.
6. на сайте гитхаб нажимаем кнопку pull request.

Fork - ответвление от изначального репозитория.
