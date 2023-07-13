## Java环境

需要Java 15及以上，Oracle JDK和OpenJDK均可。

## 安装Git

Windows需要用Git Bash。

## 安装并配置Eclipse

官方提供的版本含有Java Tutor和Constellation等插件，不过只有MIT的学生才能用，所以我直接用IDEA了。

## 命令行

常见命令包括`cd ..`, `pwd`, `ls -l`, `mkdir`, 上下箭头。

## 配置Git

1. 每次commit时Git都需要用户名和邮箱信息，因此需要提前配置
    ```
    git config --global user.name "name"
    git config --global user.email "email"
    ```
2. 可以通过创建别名方便工作，如`git lol`
    ```
    git config --global alis.lol "log --graph --oneline --decorate --color --all"
    ```
3. 查看Git配置
    ```
    git config --list
    ```

## 学习Git

包括`git clone`, `git add`, `git commit`, `git status`, `git diff`, `git diff --staged`, `git push`, `git pull`, `git log`, `git show`, `git revert`等命令，以及merge冲突的处理。
