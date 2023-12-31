## Шпралгалка по командам
### Навигация<br>
- pwd (от англ. print working directory, «показать рабочую папку») — покажи, в какой я папке;<br>
- ls (от англ. list directory contents, «отобразить содержимое директории») — покажи файлы и папки в текущей папке;<br>
- ls -a — покажи также скрытые файлы и папки, названия которых начинаются с символа .;<br>
- cd first-project (от англ. change directory, «сменить директорию») — перейди в папку first-project;<br>
- cd first-project/html — перейди в папку html, которая находится в папке first-project;<br>
- cd .. — перейди на уровень выше, в родительскую папку;<br>
- cd ~ — перейди в домашнюю директорию (/Users/Username);<br>
- cd / — перейди в корневую директорию.<br>
___
### Работа с файлами и папками<br>
- **Создание**<br>
touch index.html (англ. touch, «коснуться») — создай файл index.html в текущей папке;<br>
touch index.html style.css script.js — если нужно создать сразу несколько файлов, можно напечатать их имена в одну строку через пробел;<br>
mkdir second-project (от англ. make directory, «создать директорию») — создай папку с именем second-project в текущей папке.<br>
- **Копирование и перемещение**<br>
cp file.txt ~/my-dir (от англ. copy, «копировать») — скопируй файл в другое место;<br>
mv file.txt ~/my-dir (от англ. move, «переместить») — перемести файл или папку в другое место.<br>
- **Чтение**<br>
cat file.txt (от англ. concatenate and print, «объединить и распечатать») — распечатай содержимое текстового файла file.txt.<br>
- **Удаление**
rm about.html (от англ. remove, «удалить») — удали файл about.html;<br>
rmdir images (от англ. remove directory, «удалить директорию») — удали папку images;<br>
rm -r second-project (от англ. remove, «удалить» + recursive, «рекурсивный») — удали папку second-project и всё, что она содержит.<br>
___
### Полезные возможности
Команды необязательно печатать и выполнять по очереди. Можно указать их списком — разделить двумя амперсандами (&&).<br>
У консоли есть собственная память — буфер с несколькими последними командами. По ним можно перемещаться с помощью клавиш со стрелками вверх (↑) и вниз (↓).
Чтобы не вводить название файла или папки полностью, можно набрать первые символы имени и дважды нажать Tab. Если файл или папка есть в текущей директории, командная строка допишет путь сама.<br>
Например, вы находитесь в папке dev. Начните вводить cd first и дважды нажмите Tab. Если папка first-project есть внутри dev, командная строка автоматически подставит её имя. Останется только нажать Enter.<br>
___
### Работа с репозиторием
- git init - инициализировать репозиторий <br>
- git status - проверить статус репозитория <br>
- git add - подготовить файлы к сохранению (возможно использовать с флагом -all) <br>
- git commit -m - сделать коммит <br>
- git log - посмотреть историю коммитов <br>
- $ ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub" - генерируем ключи <br>
- $ ls -la .ssh/ # вывели список созданных ключей - проверяем созданные ключи <br>
- $ clip < ~/.ssh/id_ed25519.pub - скопировать ключ в буфер обмена <br>
- $ ssh -T git@github.com - проверяем правильность ключа<br>
- git remote add - привязать удалённый репозиторий к локальному<br>
- git remote -v - убедиться, что репозитории связаны<br>
- git push - отправить изменения на удалённый репозиторий <br>
___

### Навигация по коммитам
Для идентификации коммита используется хэш.
Кроме этой информации, в описании коммита также значится автор комиита, дата коммита и сообщение коммита.
- git log - показать список коммитов <br>
- git log --oneline - показать список коммитов в кратком виде <br>
Ссылка на последний коммит хранится в файлe _HEAD_.
___

### Статусы файлов
Статусы файлов: 
- untracked<br>
- tracked<br>
- modified<br>
- staged (indexed, cached)<br>
Чтобы узнать статус файлов в репозитории, применяется команда git status.
___

### Правила оформления сообщений к коммитам
Сообщения к коммитам должны быть короткими и информативными. Их оформление подчиняется либо правилам компании, либо общим стандартам.
В сообщении необходимо указывать номер задачи, если таковой имеется. Глаголы в сообщениях должны быть в одном времени.
___