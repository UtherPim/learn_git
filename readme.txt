Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.
Creating a new branch is quick AND simple
Git add merge （with error deal bug）

//关联远程库
# git remote add origin git@server-name:path/repo-name.git;(ssh)

//关联后，使用
git push -u origin master 第一次推送master分支的所有内容
/*
*  -u参数：git不但会把本地的master分支内容推送到远程新的master分支，还会
*把本地的master分支和远程的master分支关联起来，后续本地库如有修改，使用
* git push origin branchName 推送本地最新修改    
*/

//创建分支
#git branch branchName
//切换分支
#git checkout branchName
//切换并创建分支
#git checkout -b branchName
//查看所有分支/当前分支
#git branck (带*为当前分支)
//合并某分支到当前分支
#git merge branchName
//删除分支
#git branch -d branchName

//查看分支合并图
#git log --graph 

//使用 --no-ff 参数合并分支(git 默认使用fast forward快速合并 merge分支)
#git merge --no-ff -m "commit message" branchName
(使用--no-ff会创建一个新的commit 所以加上-m参数写入commit message)

//git 暂存(当有其他非常紧急任务时，可以暂存当前工作区)
#git stash
//回复stash至工作区
#git stash apply (恢复后stash内容不删除，需要使用git stash drop删除)
#git stash pop (恢复后stash内容删除)
//查看stash内容
#git stash list
//恢复指定工作区
#git stash apply stash@{编号}

//强制删除一个没有被合并过的分支
#git branch -D branchName