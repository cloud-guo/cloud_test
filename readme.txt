learning git
git init 初始化git仓库。
git add 文件名 向仓库添加文件。
git commit -m "comment"   把文件提交到仓库。
git status 查看当前状态
git diff 查看修改内容
git log 查看历史提交记录  --pretty=oneline参数
git reflog 查看命令历史
git reset --hard head^ 回到上一个版本  head~100 回到上一百个版本
git reset --hard commit_id 回到指定的版本。
工作区和暂存区概念
工作区：就是你在电脑里能看到的目录。
版本库：工作区有一个隐藏目录.git，这个不算工作区，而是Git的版本库。
暂存区：Git的版本库里存了很多东西，其中最重要的就是称为stage（或者叫index）的暂存区，
还有Git为我们自动创建的第一个分支master，以及指向master的一个指针叫HEAD。
把文件向版本库添加时，分为两步：
第一步是用git add把文件添加进去，实际上就是把文件修改添加到暂存区；
第二步是用git commit提交更改，实际上就是把暂存区的所有内容提交到当前分支
git checkout -- file  撤销工作区修改 命令中的--很重要，没有--，就变成了“创建一个新分支”的命令
git reset HEAD file可以把暂存区的修改撤销掉（unstage），重新放回工作区