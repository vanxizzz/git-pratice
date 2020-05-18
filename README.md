# git-pratice
git练习

工作区 -> 暂存区 -> 版本库 -> 远程仓库

- git clone
- git add 提交到暂存区
- git commit 提交到本地版本库
- git push 将本地版本库提交到远程仓库
- git status 当前提交状态
- git diff 
git diff比较的是工作区和暂存区
git diff --cached比较暂存区和版本库
git diff master 比较工作区和版本库（可切换成其他分支）


- git log 查看git日志详细信息
commit 6b221d8b.... (HEAD -> master)
提交 版本号
参数：--oneline 简化版信息


- 回退版本
git reset --hard 版本号
