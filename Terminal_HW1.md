
# Знакомство с командами Git bash

Команды использованные в данной работе:
- pwd
- cd
- mkdir
- ls
- touch
- vim
- cp/mv
- head
- tail
- less
- date
- curl
## Выполнение
Посмотреть где я
```sh
pwd
```
Создать папку
```sh
mkdir hw1
```
Зайти в папку
```sh
cd hw1
```
Создать 3 папки
```sh
mkdir hw2  hw3 hw4
```
Зайти в любоую папку
```sh
cd hw2
```
Создать 5 файлов (3 txt, 2 json)
```sh
touch f1.txt f2.txt f3.txt fj1.json fj2.json
```
Создать 3 папки
```sh
mkdir hw5 hw6 hw7
```
Вывести список содержимого папки
```sh
ls -la
```
Открыть любой txt файл
```sh
vim f3.txt
```
написать туда что-нибудь, любой текст
```sh
-i
```
сохранить и выйти.
```sh
ESC:wq
```
Выйти из папки на уровень выше
```sh
cd ..
```
переместить любые 2 файла, которые вы создали, в любую другую папку
```sh
mv {hw2/f1.txt,hw2/fj1.json} hw2/hw7/
```
скопировать любые 2 файла, которые вы создали, в любую другую папку
```sh
cp {hw2/hw7/f1.txt,hw2/hw7/fj1.json} hw3/
```
Найти файл по имени
```sh
find . -name fj2.json
```
просмотреть содержимое в реальном времени (команда grep) изучите как она работает
```sh
tail -f ../f3.txt
```
вывести несколько первых строк из текстового файла
```sh
head -n 2 ../f3.txt
```
вывести несколько последних строк из текстового файла
```sh
tail -n 2 ../f3.txt
```
просмотреть содержимое длинного файла (команда less) изучите как она работает
```sh
less FolderMoveLog.txt
```
вывести дату и время
```sh
date
```
## Выполнение запросов 
Отправить http запрос на сервер.
```sh
curl http://162.55.220.72:5005/terminal-hw-request
```
```sh
curl  -X PUST'http://162.55.220.72:5005/get_method?name=Julia&age=28'
```
## Написание скрипта
Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13
```sh
vim script.sh

#!/bin/bash
cd hw2
mkdir bh1 bh2 bh3
cd bh1
touch f_bh1.txt f_bh2.txt f_bh3.txt fj_bh1.json fj_bh2.json
mkdir bh4 bh5 bh6
ls -la
mv /c/Users/user/Testing/hw1/hw2/bh1/f_bh1.txt /c/Users/user/Testing/hw1/hw2/bh1/fj_bh1.json /c/Users/user/Testing/hw1/

chmod +x ./script.sh
./script.sh
```

