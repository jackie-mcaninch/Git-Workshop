# ACM-W Git Workshop
Welcome to the ACM-W Git Workshop! This repo can be a sandbox for you to practice all your new git skills. Below, you can find instructions on how to download Git, some handy terminal commands, and how to download and contribute to this repository! Here is the table of contents for quick navigation:
- [Git Installation](#git-installation)
- [Terminal Commands](#terminal-commands)
- [Github Account Setup](#github-account-setup)
- [Git Tutorial](#git-tutorial)
- [Further Steps](#further-steps)

## Git Installation
If you don't already have Git installed, you can find instructions for your machine at [https://git-scm.com/downloads](https://git-scm.com/downloads). For Mac and Linux, you can install it directly to an existing terminal and use from there. For Windows, it is best to download the Git Bash terminal from the website (labeled "64-bit Git for Windows Setup"). To check if you have Git previously installed, or to check that it was installed correctly, you can run the `git --version` command on your terminal (using the Git Bash terminal if you just downloaded it).

```
$ git --version
git version 2.43.0.windows.1
```

## Terminal Commands
Here are some examples of terminal commands that come up often in development. Keep these in your back pocket, it will make navigating your terminal so much easier! In the examples, any line that is preceded with a `$` is a terminal command, and the following lines are output from that command.

|Command|Description|
|---|---|
|**pwd**| print the path of the current folder
|**ls**| list all visible files in current folder
|**cd \<directory_name\>**| move into a new folder
|**touch \<file_name\>**| opens and saves a file
|**cat \<file_name\>**| displays a text file in terminal
|**man \<command\>**| displays the manual page for a command
|**vim/nano/emacs**| terminal text editor
|**[Ctrl + C]**| cancel the current running task
|**[TAB]**| autofill your current command/args

---

- ### **pwd**
This command stands for "print working directory." When running commands in terminal, you are always at some location within your file system, and `pwd` will print out the folder you are currently inside, as well as all of the folders above it.
```
$ pwd
/c/Users/jdoe
```
- ### **ls**
This command is short for "list." It will list all files in your current working directory, similar to the display you would see in your file explorer. Sometimes you will have hidden files and folders in a directory, and if you would like to see those you can run `ls -a`.
```
$ ls
 Desktop/
 Documents/
 Downloads/
 Favorites/
...
```

- ### **cd \<directory_name\>**
This command stands for "change directory." It is the same as clicking on a folder from within your file explorer. To go up one level, you can use the short hand `cd ..`, or to navigate back to your home directory you can use `cd ~`.
```
$ pwd
/c/Users/jdoe

$ cd Documents

$ pwd
/c/Users/jdoe/Documents
```

- ### **touch \<file_name\>**
This command will open the specified file, save it, and then close it. It will not allow you to edit the file. If the specified file does not exist in the current working directory, a file with that name will automatically be created and saved as an empty file.
```
$ ls
document1.txt

$ touch document2.txt

$ ls
document1.txt
document2.txt
```

- ### **cat \<file_name\>**
This command is short for "concatenate." There is a lot you can do with this command by specifying extra flags, but at the basic level you can print the contents of a file.
```
$ cat document1.txt
hello world
```

- ### **vim/nano/emacs**
These are 3 different popular terminal-based text editors. Terminals often have one of these pre-installed, and for the most part they all have the same capabilities but use different key-bindings. Similar to `touch`, you can specify an existing or new file, and it will be opened for edit.
```
$ vim document2.txt
// Terminal screen will clear and display the file contents interactively across the whole window.
```

- ### **\[TAB\]**
When in the middle of typing a file name, command, or flag, you can press the \[TAB\] key to autofill the rest if it can be inferred. For example typing `git conf` and then pressing \[TAB\] will automatically fill it in to be `git config`. If there are multiple results for the autofill, you can press \[TAB\] twice to list all possible options. For example, in the current directory, typing `cat document` and then pressing \[TAB\] twice will yield a list containing "document1.txt" and "document2.txt."

- ### **[Ctrl + C]**
This may not come up while using Git, but if running a command which is taking too long or needs to stop running for another reason, you can press [Ctrl + C] to stop the current running process. **WARNING: while in terminal you cannot use [Ctrl + C] to copy text!**

## Github Account Setup

## Git Tutorial

## Further Steps