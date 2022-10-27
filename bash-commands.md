# Шпаргалка по консольным командам Bash (PowerShell)

# Перемещение в домашний каталог
cd
cd ~ # домашняя директория

# Переход в системную папку
cd ~/Desktop

cd .. # Переход на один уровень выше
cd - # Переход к последней рабочей папки

# Переход в папку
cd <folder>
cd first-folder # Переход в каталог first-folder, которая есть текущей папке
cd first-folder/sub-folder # Перемещение в каталог sub-folder по указанному пути

cd /c # Переход в корень диска c
cd /d # Переход в корень диска d
cd /d/Projects # Переход в папку Projects, расположенную по адресу d:/Projects

# Получить путь текущей папки
# pwd - сокращенно print working directory
pwd

# Создать папку
mkdir <folder>

mkdir my-project 
mkdir my-project/sub-folder # создать подпапку не переходя в главную папку
mkdir sub-folder-1 sub-folder-2 sub-folder-3 # Создать несколько папок
mkdir my-project my-project/sub-folder-1 my-project/sub-folder-2
mkdir -p my-project/{sub-folder-1,sub-folder-2}

# Удалить папку
rmdir <folder>
rmdir demo
rmdir my-project/subfolder # удалить подпапку app-demo находясь в верхнем каталоге my-project
rmdir -v sub-folder # при удалении папки отображать сообщение об удалении
rmdir sub-folder-1 sub-folder-2 sub-folder-3 # Удалить 3 папки

# Например, у вас 3 каталога - subfolder1 subfolder2 subfolder3.
# Используйте маску "*", что бы удалить все каталоги 
rmdir sub-folder* 

# Создать пустой файл
touch <file>
touch readme.md



# Создать файл с текстом
echo "Some text" > file.txt

``` bash
# Просмотреть список файлов в папке
ls
ls -la
cd /d/Projects # Показать содержимое папки d:/Projects
```

# Чтение файла
cat <file>
cat file.txt

# Удаление файла
rm <file>
rm file.txt

# Удаляем все непустые папки folder-name/sub-folder-1 folder-name/sub-folder-2 folder-name/sub-folder-3
# "-r" (R) - флаг удалит все подпапки или файлы в этой конкретной папки.
# "f" - флаг используется для принудительного удаления этой папке без отображения запроса.
# "v" - флаг используется для отображения процесса удаления папки с текстовым выводом.
rm -r folder-name 
rm -rf folder-name
rm -rfv folder-name 

# Разное

clear # очистить консоль
echo Hello World # Команда echo - выводит текст на консоль.
echo "Some text" # Команда echo - выводит текст на консоль.
whoami # выводит имя пользователя