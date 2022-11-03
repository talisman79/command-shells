# Шпаргалка по консольным командам Bash (PowerShell)

## Перемещение в домашний каталог
``` bash
cd
cd ~ # домашняя директория
```

## Переход в системную папку
``` bash
cd ~/Desktop
cd .. # Переход на один уровень выше
cd -  # Переход к последней рабочей папки
```

## Переход в папку
``` bash
cd <folder>
cd first-folder # Переход в каталог first-folder, которая есть текущей папке
cd first-folder/sub-folder # Перемещение в каталог sub-folder по указанному пути
cd /c # Переход в корень диска c
cd /d # Переход в корень диска d
cd /d/Projects # Переход в папку Projects, расположенную по адресу d:/Projects
```

## Получить путь текущей папки
>pwd - сокращенно print working directory
``` bash
pwd
```

## Создать папку
``` bash
mkdir <folder>
mkdir my-project 
mkdir my-project/sub-folder # создать подпапку не переходя в главную папку
mkdir sub-folder-1 sub-folder-2 sub-folder-3 # Создать несколько папок
mkdir my-project my-project/sub-folder-1 my-project/sub-folder-2
mkdir -p my-project/{sub-folder-1,sub-folder-2}
```

## Удалить папку
``` bash
rmdir <folder>
rmdir demo
rmdir my-project/subfolder # удалить подпапку app-demo находясь в верхнем каталоге my-project
rmdir -v sub-folder # при удалении папки отображать сообщение об удалении
rmdir sub-folder-1 sub-folder-2 sub-folder-3 # Удалить 3 папки
```

Например, у вас 3 каталога - subfolder1 subfolder2 subfolder3.  
Используйте маску "*", что бы удалить все каталоги.
``` bash
rmdir sub-folder* 
```

## Создать пустой файл
``` bash
touch <file>
touch readme.md
```

## Создать файл с текстом
``` bash
echo "Some text" > file.txt
```

## Просмотреть список файлов в папке
``` bash
ls
ls -la
cd /d/Projects # Показать содержимое папки d:/Projects
```

## Чтение файла
``` bash
cat <file>
cat file.txt
```

## Удаление файла
``` bash
rm <file>
rm file.txt
```

Удаляем все непустые папки **folder-name/sub-folder-1 folder-name/sub-folder-2 folder-name/sub-folder-3**  
**-r** (R) - флаг удалит все подпапки или файлы в этой конкретной папки.  
**f** - флаг используется для принудительного удаления этой папке без отображения запроса.  
**v** - флаг используется для отображения процесса удаления папки с текстовым выводом.
``` bash
rm -r folder-name 
rm -rf folder-name
rm -rfv folder-name 
```

## Разное
``` bash
clear # очистить консоль
echo Hello World # Команда echo - выводит текст на консоль.
echo "Some text" # Команда echo - выводит текст на консоль.
whoami # выводит имя пользователя
```