1. ***whoami*** - Print the user name associated with current effective user id.
2. ***man*** - it stands for manual and prints all the information related to that command
3. ***clear*** - used to clear the terminal, shortcut method is ctrl + l.
4. ***pwd*** - stands for path of the working directory. print the name of the current working directory
5. ***ls*** - inside a folder you can list all the files that the folder contains	
	- if you add a folder name or path, it will print that folder contents like `ls Downloads`
	- it accepts a lot of option and a very useful option is `ls -al Downloads`, this print all the details about the file and this is done by **l** and **a** is used to show all the hidden files
7. ***cd*** - it helps to move control to a directory
	- cd command is implemented by the shell and it has no manual page
	- there is a different command that is `help cd`, this is the shell version of the `man cd`
	- you can also come back from a directory using `cd ..`
	- again you can also use it in nested way `cd ../..` to come back from nested folders
	- you can jump as many levels as you want just by writing `cd shraddha/a/`, and this will take to the the folder **a** that is inside the folder **shraddha**
	- again you can do same thing for backward,  just write `cd ../../`
8. ***mkdir*** - stand for make directories, used to create folders and stuff, you can make multiple folders at a time like `mkdir a b c`, it will create 3 folders named as a, b and c
	- **-p** used to make parent directories as needed
	- **-v** - print a message for each created directory
	- you can also give it some destination to make a folder anywhere without changing the current working directory
9. ***touch*** - this is used to create empty files if the given name is not exist 
	- if the file exist it will update its time stamp without changing the existing data of the file
10. ***rmdir*** - this stands for remove directories, you can delete single or multiple directories(separated by spaces), and remember this will only work if the *folder is empty*
	- *there is no bin while removing files from the command line and recovering lost files can be extremely hard*
11. ***rm*** - it stands for remove, it helps to remove files and directories 
	- **-v** used to give the feedback when we perform any type of the operation
	- again we cant delete a folder with something in it directly using rm, we have to use a flag to remove it
	- **-r** this flag stands for recursive, this helps to remove directories recursively 
	- **-i** this flag stands for interactive and this is very useful, this ask us to give our opinion to delete a file or not, so try to use this flag along with **r** before deleting directories
12. ***xdg-open*** - open an file using terminal