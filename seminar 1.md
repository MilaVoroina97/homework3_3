# Инструкция по работе с Git
 
## 1. Начало работы с Git

## 2. Основные команды для работы с Git
 
## 3. Лайфхаки по работе с командами Git

## 4. Работа с удаленными репозиториями

- ### Начало работы с Git ###

Для начала работы с Git. Необходимо скачать и настроить саму программу Git и программу *Visual Studio Code*. Ссылки на скачивание программ и подробная инструкция по их настройке Вы можете найти здесь: [Git](https://git-scm.com/book/ru/v2/Введение-Установка-Git) | [VS Code](https://code.visualstudio.com)


После настройки и скачивания программ Git и VS Code необходимо создать пустую папку на рабочем столе и открыть VS Code. Затем открыть эту папку через пункт меню *Проводник*. Далее открыть *Терминал* и представиться гиту с помощью команд:

- **git config --global user.name «Ваше имя английскими буквами»**
- **git config --global user.email ваша почта@example.com**

И запускаем следующую команду для работы Git :  ***git init***.
Данная команда иницилизирует работу Git и позволяет нам начать отслеживать все действия, происходящие в папке.
Давайте рассмотрим также все основные команды Git в следующем разделе.


- ### Основные команды в Git ###

***git status*** - показывает текущее состояние гита, есть ли какие-то действия, которые нужно сохранить.

![Как выглядит команда](git%20status.jpg)

***git add*** - позволяет добавить отслеживание изменений в рабочий файл. Для работы команды необходимо указать название файла, который нужно добавить в отслеживание.

![Как выглядит команда](git%20add.jpg)

***git commit*** - сохраняет все изменения, которые были сделаны в рабочем файле. Для сохранения нужно вызвать команду и обязательно указать сообщение об изменении:

![Как выглядит команда](git%20commit.jpg)

***git log*** - показывает весь журнал изменений, происходящих в рабочем файле, а также показывает список всех коммитов:


![Как выглядит команда](git%20log.jpg)

***git checkout*** - позволяет переключаться между разными версиями файла, возвращаться к ранее сохраненной версии и так далее. Для этого необходимо вести данную команду и написать первые четыре символа нужного Вам коммита: 

![Как выглядит команда](git%20checkout.jpg)

***git diff*** - показывает разницу между текущим файлом и тем, который мы сохранили:

![Как выглядит команда](git%20diff.jpg)

***git reflog*** - показывает список всех коммитов в сокращенном виде:

![Как выглядит команда](git%20reflog.jpg)

- ### Лайфхаки по работе с командами Git ###

***git commit -am"your comment"*** - сочетает в себе сразу две команды *git add + git commit*:

![Как выглядит команда](git%20add+commit.jpg)

***git add .*** - если создано много файлов или внесено много изменений к ним, то тогда можно использовать эту команду.

Данная команда добавить в отслеиживание все файлы, в которых были изменения, а также все новые файлы.

- ### Работа с удаленными репозиториями ###

Для того чтобы участовать в Open Sourse проектах, а также работать и принимать участие в любых других проектах на GitHub нужно уметь пользоваться удаленными репозиториями.

Здесь я пишу краткую инструкцию по работе с удаленными репозиториями и основные команды, которые помогут Вам научиться работать с удаленными репозиториями:

1. Для начала надо зарегистировать свой аккаунт на GitHub (https://github.com/), если у Вас еще его нет.

2. После Вам необходимо "подружить" GitHub и VS Code, а именно в VS Code найти в левом нижнем углу круглую иконку с человечком, нажать на нее и выбрать синхронизацию, в выпадающем меню выбрать вариант синхронизации с GitHub. Обратите внимание, что при этом у Вас должен быть открыть профиль на GitHub в выбранном по умолчанию браузере на компьютере.

2. Далее заходим в свой профиль и создаем новый репозиторий для работы с ним. Находим пункт меню **Repositories** и нажимаем зеленую кнопку **New**:

![Создание репозитория](git%20photo1.jpg)


3. После создания репозитория следуем дальнейшим инструкциям GitHub и пишем в VS Code следующие три комады:

 - ***git remote add origin https://github.com/Name_of_GitHub_account/Name_of_repozitiry.git***

 - ***git branch -M main***

 - ***git push -u origin main***

Данные команды позволят нам выгрузить свою работу/свой код, который мы писали локально в VS Code  выгрузить на GitHub и уже любой другой пользователь GitHub может увидеть Вашу работу.

4. Для того чтобы выгрузить свои измения из локального репозитория в удаленный репозиторий (GitHub) используйте команду ***git push***

И наоборот, если Вы делалете какие - то изменения на удаленном репозитории и хотите увидеть эти изменения в VS Code используйте команду ***git pull***.

5. Далее изучим команду ***pull request***. Данная команда необходима, для того чтобы Вы могли предложить какие -то свои изменения в работы и проекты на GitHube других пользователей:

- Для того чтобы сделать *pull request* необходимо сначала найти открыть репозиторий с папками инстрисуемого Вами проекта и нажать ***Fork*** в правом верхнем углу:

![Fork](git%20photo2.jpg)

- Далее необходимо найти зеленую кнопку ***Code***, нажать на нее и скопировать ссылку в HTTPS, которая выдается при нажатиии:

![Code](git%20photo3.jpg)

- И далее нам необходимо вернуться обраться в VS Code и с помощью команды ***git clone*** + ссылка на репозиторий(которую мы скопировали из Code) скопировать этот репозиторий себе локально.

- После этого с помощью команды ***cd*** + имя папки нужно перейти в папку удаленного репозитория, чтобы там предложить свои изменения.

- **!!Следующий важный шаг - это создать НОВУЮ ВЕТКУ!!** и только после этого можно вносить изменения в проект.

- После того, как мы закончили вносить изменения необходимо "запушить" все эти изменения на удаленный репозиторий с помощью команды ***git push***. Но перед пушем не забудьте сохранить все изменения с помощью команды ***git commit***

- Далее переходим в GitHub, с ветки main переходим на ветку, которую Вы создали и в которой Вы внесли изменения, и видим, что появилась кнопка ***Compare & pull request*** :

![Compare & pull request](git%20photo4.jpg)

- Нажимаем на эту кнопку, создаем Pull request, оставляем комментарий владельцу репозитория об изменениях, которые мы хотим ему предложить и нажимаем кнопку ***Create pull request***.

На этом все!