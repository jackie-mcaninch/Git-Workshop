# ACM-W Git Workshop
Welcome to the ACM-W Git Workshop! This repo can be a sandbox for you to practice all your new Git skills. Below, you can find instructions on how to download Git, some handy terminal commands, and how to download and contribute to this repository! Here is the table of contents for quick navigation:
- [Git Installation](#git-installation)
- [Terminal Commands](#terminal-commands)
- [Git Tutorial](#git-tutorial)
- [Extended Terminal Commmand Examples](#extended-terminal-command-examples)

## Git Installation
If you don't already have Git installed, you can find instructions for your machine at [https://git-scm.com/downloads](https://git-scm.com/downloads). For Mac and Linux, you can install it directly to an existing terminal and use from there. For Windows, it is best to download the Git Bash terminal from the website (labeled "64-bit Git for Windows Setup"). To check if you have Git previously installed, or to check that it was installed correctly, you can run the `git --version` command on your terminal (using the Git Bash terminal if you just downloaded it).

```
$ git --version
git version 2.43.0.windows.1
```

## Terminal Commands
Here are some examples of terminal commands that come up often in development. Keep these in your back pocket, it will make navigating your terminal so much easier! You can find examples for each at the end of the document.

|Command|Description|
|---|---|
|[**pwd**](#pwd)| print the path of the current folder
|[**ls**](#ls)| list all visible files in current folder
|[**cd \<directory_name\>**](#cd-directory_name)| move into a new folder
|[**touch \<file_name\>**](#touch-file_name)| opens and saves a file
|[**cat \<file_name\>**](#cat-file_name)| displays a text file in terminal
|[**vim/nano/emacs**](#vimnanoemacs)| terminal text editors
|[**\[Ctrl + C\]**](#ctrl--c)| cancel the current running task
|[**\[TAB\]**](#tab)| autofill your current command/args

## Git Tutorial
Here are the steps for creating your own clone of this repository, where you can make your own branch and edits. You can clone and edit locally without a Github account, but in order to push to the repository, you must create an account. Please make sure not to skip any steps!

### Step 1: **Fork the repository**
This repository belongs to a personal account, and contributions cannot be made by anyone except those directly added to the project. Since there are many unknown collaborators, it is best for you to make a copy of this remote repository, which is called a **fork**. This will be yours and you can change it in whatever way you please!

- In the "Code" tab of this project, click the "Fork" button in the top right
- On the fork page, click "Create fork" (you don't need to change anything).
- If you aren't already there, navigate to this new repo in your profile
- Confirm that the repo you are on is named "\<your-username\>/Git-Workshop"

### Step 2: **Clone the repository**
In order to get this remote (web-based) repository onto your local machine, you will need to clone the repository. Again, confirm that the page you are on is YOUR fork!
- Click the green drop-down "Code" button
- Select HTTPS and copy the address of the repo
- Open terminal and navigate to the folder where you would like to store your local repo
- Clone the repository using the address you just copied **(note: using [Ctrl + V] may not work)**
- Move into the new folder named "Git-Workshop"
```
$ git clone https://github.com/your-username/Git-Workshop.git
$ cd Git-Workshop
```

### Step 3: **Set up configuration**
In professional software development, it is critical for other developers to know who authored commits on a repo. You will need to denote what your user name and email are ahead of time in order for them to be included on your commits.
- Set your user.name to be your github username
- Set your user.email to be your email (generally the one associated with Github)
```
$ git config --global user.name "your-username"
$ git config --global user.email "your-email"
```

### Step 4: **Create a new branch**
When creating new features, it is important to keep them separate from the main branch in order to avoid interfering with the main branch. This is because new features often create new problems as well. You can name this branch whatever you want, but try to make it descriptive. Since this exercise is for exploration purposes, a good name could be "sandbox."
- Create a new branch copied from the main branch
- To confirm we are on the right one, list all active branches with `git branch`
```
$ git checkout -b <your-branch-name>
$ git branch
```

### Step 5: **Make some edits**
This is where you get to be creative and have a little freedom. You can create new files, edit existing files, or even remove existing files. Make sure that once you are done editing files, **SAVE THEM**! If you add the file to the staging area, it will only stage the saved changes.

### Step 6: **Add changes to the staging area**
Remember, staging changes means you are *choosing* which changes to include in your commit. You will probably want to include them all. If you removed a file, this file will only be removed in the next commit, it will still exist inside all the previous commits. The example below assumes that the coder has made changes to 3 python files, and wants to remove the README. But for you, it is better to keep it. :\)
- Add the changes you would like to include in the next snapshot
- For any files that you would like to delete for the next commit, use `git rm`
```
$ git add test1.py test2.py test3.py
$ git rm README.md
```

### Step 7: **Commit the changes**
This step is going to wrap up all the changes we have staged into one commit, dated at the current time stamp and marked with your user name and email. It is also a good idea to make your commit messages brief but specific. If there is too much to explain on one-line, you probably should break up the commit into multiple.
- Commit the staged changes with a message
```
$ git commit -m "a descriptive message about your changes"
```

### Step 8: **Push the changes**
Now that you have all your new changes packaged up and ready to share, you need to publish them to your remote repo so that everyone can see it. It is possible to have multiple remotes (destinations to store your code), but in this case we haven't added any so our only remote is `origin`, the one we cloned from. Secondly, you need to specify what remote branch to push to, which should match the local branch name even if it does not exist on the remote yet.
- Push the new commit(s) to your remote repository
```
git push origin <your-branch-name>
```
---
Congratulations, you've finished the Git tutorial! To keep developing, repeat steps 5-8 and make new branches as necessary. Well done, you're now an ACM-W certified Git Ninja!


<div style="text-align: center;">
    <img width="400" src="acmw-logo.png">
</div>

 
 
## Extended Terminal Command Examples
Here are some more examples of the usage for the commands listed previously. In the examples, any line that is preceded with a `$` is a terminal command, and the following lines are output from that command.

---
- ### **pwd**
This command stands for "print working directory." When running commands in terminal, you are always at some location within your file system, and `pwd` will print out the folder you are currently inside, as well as all of the folders above it.
```
$ pwd
/c/Users/jdoe
```
---
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
---
- ### **cd \<directory_name\>**
This command stands for "change directory." It is the same as clicking on a folder from within your file explorer. To go up one level, you can use the short hand `cd ..`, or to navigate back to your home directory you can use `cd ~`.
```
$ pwd
/c/Users/jdoe

$ cd Documents

$ pwd
/c/Users/jdoe/Documents
```
---
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
---
- ### **cat \<file_name\>**
This command is short for "concatenate." There is a lot you can do with this command by specifying extra flags, but at the basic level you can print the contents of a file.
```
$ cat document1.txt
hello world
```
---
- ### **vim/nano/emacs**
These are 3 different popular terminal-based text editors. Terminals often have one of these pre-installed, and for the most part they all have the same capabilities but use different key-bindings. Similar to `touch`, you can specify an existing or new file, and it will be opened for edit.
```
$ vim document2.txt
// Terminal screen will clear and display the file contents interactively across the whole window.
```
---
- ### **\[TAB\]**
When in the middle of typing a file name, command, or flag, you can press the \[TAB\] key to autofill the rest if it can be inferred. For example typing `git conf` and then pressing \[TAB\] will automatically fill it in to be `git config`. If there are multiple results for the autofill, you can press \[TAB\] twice to list all possible options. For example, in the current directory, typing `cat document` and then pressing \[TAB\] twice will yield a list containing "document1.txt" and "document2.txt."

- ### **[Ctrl + C]**
This may not come up while using Git, but if running a command which is taking too long or needs to stop running for another reason, you can press [Ctrl + C] to stop the current running process. **WARNING: while in terminal you cannot use [Ctrl + C] to copy text!**