# git-pratice

git练习

工作区 -> 暂存区 -> 版本库 -> 远程仓库

## 基本操作
- 克隆远程仓库
git clone

- 提交内容到暂存区
git add 

- 提交到本地版本库
git commit 

- 将本地版本库提交到远程仓库
git push 

- 当前提交状态
git status 

- 比较内容差异 
git diff比较的是工作区和暂存区
git diff --cached比较暂存区和版本库
git diff master 比较工作区和版本库（可切换成其他分支）


- 查看git日志详细信息
git log
commit 6b221d8b.... (HEAD -> master)
提交 版本号 (当前指针 )
参数：--oneline 简化版信息

git log --graph --pretty=oneline --abbrev-commit


- 回退版本（撤销本次提交）
git reset --hard 版本号
如：git reset --hard 6b221d

- 查看操作记录
git reflog

- 撤销操作
1. 回退版本
2. 撤销工作区的文件内容
如：git checkout test.html或git checkout .
3. 撤销存放在**暂存区**的内容
git reset HEAD test.html或git reset HEAD .

- 删除文件
1. 删除暂存区 + 工作区
git rm -f test.html或git rm -f .
2. 删除暂存区
git rm --cached test.html


## 远程仓库
- 查看仓库名
git remote

- 查看仓库地址
git remote -v

- 修改仓库名（origin变成newOrigin）
git remote rename origin newOrigin

- 添加远程仓库
git remote add 新仓库名 仓库地址
如：git remote add origin http://xxxx

- 删除仓库
git remote rm 仓库名

- push代码到远程仓库
git push 仓库名 分支
如：git push origin master

## 分支

假设当前mster指向的版本号： 92437f...

1. 分支快速合并(Fast-Forword)：（直接把master指针指向dev提交的版本号a344ddc）
（将master的指针直接移动到了分支所新创建的版本上）
（假设当前是在dev分支）
git commit -m "dev"(版本号：a344ddc....)
git checkout master
**git merge dev** 
**HEAD 👉 master 👉 a344ddc....  👈 dev**

         （master）
            👇
92437f 👈 a344ddc 
            👆
          （dev）

2. 非快速合并：（即master指针不是指向dev提交的版本号，而是指向一个新的版本号）

...
**git merge --no-ff dev -m "修复"**（产生一个新的版本号：90b23e...）


         （master）
            👇
92437f ← 90b23e 
↑          ↓
a344ddc ←←←← 
👆
（dev）
    


## 注意事项
1. 切换分支前一定要commit或stash