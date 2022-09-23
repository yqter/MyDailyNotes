# Git的使用经验

## 01 创建自己的名字和邮箱

`git config --local user.name`  "你的用户名"

`git config --local user.email` "你的邮箱"

只有该项目才有用

将 `--local` 换成 `--global` 就变成全局了

## 02 生成一个新仓库

克隆一个已经存在的仓库

`git clone ssh`

生成一个新的本地仓库

`git init`

## 03 本地仓库的操作

`git status` 可以查看目前文件的状态。是已经被提交了还是处于其他状态。

`git diff FirstGit.c` 查看当前没有add的内容；查看修改了什么内容。//与暂存区中的做对比。

`git add .` 将目前文件夹里所有的更改都add进暂存区。

`git add -p <file>` 将某文件中的改变添加到暂存区

`git commit -m "my first"`  告诉Git，把文件**提交**到仓库，后附上本次提交的说明。

实际上就是把暂存区的所有内容提交到当前分支

## 03 关联远程库

如果是想关联github的话，首先需要创建一个ssh密匙

```bash
ssh-keygen -t rsa -C "youremail@example.com"
```

将产生的密匙文件，pub结尾的文件内的的内容复制进github里面。

然后进入库里复制它的ssh链接

后面

```bash
git remote add origin git@github.com:you/project.git
```

origin是自定义的名字，可以自己随便决定一个哦。

## 04 分支

`git branch <new name>` 创建一个新分支

`git checkout <name>` 切换到新的分支

`git branch -d <name>` 删除这个分支

`git branch -m <old name> <new name>` 更改分支名称

`git checkout -b <new name>` 新建分支并转入

`git branch` 查看本地分支 

`git branch -r` 查看远程分支

`git branch -a` 查看 本地+远程

## 05 推送

`git push <name> <分支名>` 推送本地仓库到远程仓库的什么什么分支。

`git fetch` 如果远程仓库出现了别的修改，你可以靠这个命令发现。然后决定要不要用 `git merge` 将你现在所处的分支合并。

`git merge origin/master` 这句话的意思是，将`origin`这个远程端的`master`分支与你现在所处的分支合并。
