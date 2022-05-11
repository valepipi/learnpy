#创建分支dev
git branch dev

#切换到dev分支
git checkout dev
#或者
git switch dev

#创建并切换分支
git checkout -b dev
#或者
git switch -c dev


#查看当前分支
git branch

#在dev分支上工作
#将修改后的文件，从工作区加入到暂存区，准备提交
git add readme.txt
#将暂存区的文件提交，并备注一些信息
git commit -m "branch test"

#返回master分支
git checkout master

#将dev分支合并到master分支
git merge dev

#合并后，即可删除dev分支
git branch -d dev

#使用分支完成某个任务，合并后再删除分支
#这和直接再Master分支上工作效果一样，但过程更安全

#以上合并方式为fast forward，无法看出合并历史
#以下合并方式，禁用ff，可以看出合并历史
git merge --no-ff -m "merge with no-ff" dev

#查看历史分支
git log --graph --pretty=oneline --abbrev-commit


#多人协作

#对方
#克隆库
git clone ...

#查看远程库信息
git remote -v

#git branch查看分支
#若在dev上协作开发，若本地五dev分支，则创建远程origin的dev分支到本地
git checkout -b dev origin/dev

#git add ...
#git commit -m "..."
#git push origin dev


#自己
#若本地有dev分支，则指定本地dev分支与远程Origin/dev分支的链接
git branch -set-upstream-to=origin/dev dev

#pull下来
git pull

#解决合并冲突

#提交，push
git commit -m "..."
git push origin dev

