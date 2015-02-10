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
远程操作
git remote add origin 远程仓库地址  关联远程库
git push -u origin master 第一次向远程库推送master分支的所有内容
git push origin master 向远程库推送最新修改
git clone 远程库地址  克隆一个本地库
git checkout -b 分支名称  创建分支并切换到该分支
git branch 命令会列出所有分支，当前分支前面会标一个*号
git merge 指定分支名 把指定分支合并到当前分支Fast forward模式
git branch 分支名 创建分支
git branch -d 分支名 删除该分支
git log --graph --pretty=oneline 命令可以看到分支合并图
git merge --no-ff <name> 合并分支禁用Fast forward模式
合并分支时，加上--no-ff参数就可以用普通模式合并，合并后的历史有分支，能看出来曾经做过合并，而fast forward合并就看不出来曾经做过合并。
git stash 把当前工作现场“储藏”起来，等以后恢复现场后继续工作
git stash list 查看当前存储的工作
git stash apply 恢复当前存储的工作
git stash drop 删除stash内容
git stash pop 恢复同时把stash内容也删了
git branch -D <name> 强行删除没有合并的分支
git remote -v 显示远程仓库详细的信息
git checkout -b <name> <name> 在本地创建和远程分支对应的分支，本地和远程分支的名称最好一致；
git branch --set-upstream <name> <name>指定本地分支与远程分支的链接
多人协作冲突解决步骤：
首先，可以试图用git push origin branch-name推送自己的修改；
如果推送失败，则因为远程分支比你的本地更新，需要先用git pull试图合并；
如果合并有冲突，则解决冲突，并在本地提交；
没有冲突或者解决掉冲突后，再用git push origin branch-name推送就能成功！
如果git pull提示“no tracking information”，则说明本地分支和远程分支的链接关系没有创建，
用命令git branch --set-upstream <name> <name>
标签：
git tag <name> 创建标签
git tag 查看所有标签
git tag <name>  <commit id>  创建历史版本标签
git tag -a <tagname> -m "blablabla..."可以指定标签信息；
git tag -s <tagname> -m "blablabla..."可以用PGP签名标签；
git show <tagname>查看标签信息
git push origin <tagname>可以推送一个本地标签；
git push origin --tags可以推送全部未推送过的本地标签；
git tag -d <tagname>可以删除一个本地标签；
git push origin :refs/tags/<tagname>可以删除一个远程标签。