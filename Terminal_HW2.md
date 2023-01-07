
# Git bash part 2

Commands used in this task:
- pwd
- cd
- mkdir
- ls
- touch
- vim
- cp/mv
- head
- tail
- cat
- find
- grep
## Execution
Create a folder dir_1
```sh
mkdir dir_1
```
Go to the folder dir_1
```sh
cd dir_1
```
Create a folder inner_dir_1 
```sh
mkdir inner_dir_1
```
Print the current directory
```sh
pwd
```
Create an empty text file from the dir_1 folder tf_1.txt
```sh
touch tf_1.txt
```
Create the text file tf_2.txt with the following lines from the cat command in the dir_1 folder:
- the first 1
- the second 2
- the third 3
```sh
cat > tf_2.txt CTRL^C
```
Go to the folder inner_dir_1 
```sh
cd inner_dir_1
```
Using cat make text file tf_3.txt with any strings
```sh
cat > tf_3.txt CTRL^C
```
Add "the second 2" to the tf_3.txt text file using cat
```sh
cat >> tf_3.txt CTRL^C
```
Add "the sec 2" to the tf_3.txt text file using cat
```sh
cat >> tf_3.txt CTRL^C
```
Add "the sec 3" to the tf_2.txt text file via cat
```sh
cat >> ../tf_2.txt CTRL^C
```
Add "the SeCoNd 2" to the tf_3.txt text file via cat
```sh
cat >> tf_3.txt CTRL^C
```
Add "the seConD 2" to the tf_2.txt text file via cat
```sh
cat >> ../tf_2.txt CTRL^C
```
Create a text file tf_4.txt with 15 lines.
```sh
vim tf_4.txt i 15 Enter esc :wq
```
Create a text file tF_5.txt with 13 lines.
```sh
vim tF_5.txt i 13 Enter esc :wq
```
Lists all files in a folder
```sh
ls */*
```
Exit Folder inner_dir_1
```sh
cd ..
```
Displays the contents of the tf_3.txt file in the terminal
```sh
cat inner_dir_1/tf_3.txt
```
Displays the contents of the tf_3.txt file in the terminal. tf_4.txt 
```sh
find ~/dir_1 -name tf_4.txt
```
Remove the tf_4.txt file from the content without deleting the file itself
```sh
> inner_dir_1/tf_4.txt
```
Find the path to files that have a "tf" in the name
```sh
find -name "tf*"
```
Find the path to files that have a "tf" in the title and letters in any case
```sh
find -iname "tf*"
```
Find strings in files where there is a "sec" combination in the current folder
```sh
grep sec *
```
Find strings in files where there is a "sec" combination in any case in the current folder
```sh
grep -i sec *
```
Find strings in files where there is only a "sec" combination in the current folder
```sh
grep -w sec *
```
Find strings in files where there is only a "sec" combination in any case in the current folder
```sh
grep -wi sec *
```
Find strings in files where there is com. binging the letters "second" in the current folder
```sh
grep second *
```
Find strings in files where there is a "second" combination in any case in the current folder
```sh
grep -i second *
```
Найти строки в файлах где есть комбинация букв “second” во всех папках ниже уровнем
```sh
grep -r "second" ./*/
```
Find strings in files where there is a "second" combination in all folders below the level
```sh
grep -l second *
```
Find all strings in all files where there is no "second" combination
```sh
grep -vr second
```
Find only name and file path where there is no "second" combination
```sh
grep -rL second *
```
Display the last 4 lines of any text file
```sh
tail -n 4 inner_dir_1/tF_5.txt
```
Print the first lines of any text file in Terminal 4.
```sh
head -n 4 inner_dir_1/tF_5.txt
```
Command in one line. Create a folder and create a text file with the contents.
```sh
mkdir inner_dir_2 | echo hello > file.txt
```
Command in one line. Move to any single folder text files that have the word "sec" in the content
```sh
grep -wlr "sec" . | xargs mv -t inner_dir_2
```
Command in one line. Copy to any single folder text files that have the word "sec" in the content
```sh
grep -wlr "sec" . | xargs cp -t inner_dir_1
```
Command in one line. Find all strings with "sec" in all text files, copy and paste these strings into one newly created text file.
```sh
grep -rh "sec" > new.txt
```
Command in one line. Delete text files that have the word "sec" in their content
```sh
grep -wlr "sec" . | xargs rm
```
Simply display the line "Good job!"
```sh
echo "Good job\!\!"
```