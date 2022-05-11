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
