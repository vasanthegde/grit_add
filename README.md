# git-add
It is simple CLI tool for your **_git add_** command.

there are great tools like lazygit or gitui which provides so far better fetaures for git commands. 
If you are looknig for full blown git integration please go to such tools.

then why this yet another tool ?
I am simple man and most of the time I use following git workflow in terminal
1. git status 
2. git add
3. git commit
4. git push

the main problem with "git add" command is it need complete file path which is bit annoying. 
Hence this tiny CLI wrapper which takes shorthand or simple file names as input and executes git add command to matching unstaged files. 
No need to remember any keyboard shortcuts. 

# Guide 
1. 
```
./git-add
```
which will prompt label to user to select which file to be added
![image](https://user-images.githubusercontent.com/12895102/211626465-95b8009f-bea5-4943-8a8c-b728da5a5711.png)

2.
```
./git-add lib.rs
```
which will match **src/lib.rs** and execute git add **src/lib.rs** command

3.
```
./git-add file
```
which will match two files **file1.txt** and **file2.txt** and prompt lable input to execute git add command
![image](https://user-images.githubusercontent.com/12895102/211627064-70ad0a18-841b-4cec-b712-e5a07c7c2277.png)

4.
```
./git-add MGAF 
```
which will match file with name **MyGlobalAbstractFactory.java** for example.

5.
```
./git-add MGAF lib.rs main.rs
```
you can pass multiple file names at once

## Installation
If you would like to build from source:

```
git clone https://github.com/vasanthegde/git-add
cd git-add
cargo install --path .
```
else checkout release section to grab available binaries.


## Upcoming features
1. performance optimazation by using hashmap look ups
2. color coded user prompts ( green for added files, yellow for modified and red for deleted files ) 
3. perhaps more file matching pattern
