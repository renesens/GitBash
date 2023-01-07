
# Commands used in this task:
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
Display current location
```sh
pwd
```
Create a folder
```sh
mkdir hw1
```
Go to a folder
```sh
cd hw1
```
Create 3 Folders
```sh
mkdir hw2  hw3 hw4
```
Go into any folder
```sh
cd hw2
```
Create 5 files (3 txt, 2 json)
```sh
touch f1.txt f2.txt f3.txt fj1.json fj2.json
```
Create 3 folders
```sh
mkdir hw5 hw6 hw7
```
List the contents of the folder
```sh
ls -la
```
Open any txt file
```sh
vim f3.txt
```
Write any text
```sh
-i
```
Save and exit
```sh
ESC:wq
```
Exit folder to the level above
```sh
cd ..
```
Move any 2 files you created to any other folder
```sh
mv {hw2/f1.txt,hw2/fj1.json} hw2/hw7/
```
Copy any 2 files you have created to any other folder
```sh
cp {hw2/hw7/f1.txt,hw2/hw7/fj1.json} hw3/
```
Find File by Name
```sh
find . -name fj2.json
```
View content in real time (grep command) learn how it works
```sh
tail -f ../f3.txt
```
Print the first few lines from the text file
```sh
head -n 2 ../f3.txt
```
Output a few last lines from the text file
```sh
tail -n 2 ../f3.txt
```
View the contents of a long file (less) Learn how it works
```sh
less FolderMoveLog.txt
```
Print date and time
```sh
date
```
## Execution of queries
Send http request to server.
```sh
curl http://162.55.220.72:5005/terminal-hw-request
```
```sh
curl  -X PUST'http://162.55.220.72:5005/get_method?name=Renata&age=38'
```
## Writing scripts
Write a script that will automatically execute items 3, 4, 5, 6, 7, 8, 13
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

