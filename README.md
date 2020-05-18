# git-pratice
git练习

工作区 -> 暂存区 -> 版本库 -> 远程仓库

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


- 回退版本（会改变工作目录）
git reset --hard 版本号
如：git reset --hard 6b221d

- 查看操作记录
git reflog

- 撤销操作
1、回退版本
2、



