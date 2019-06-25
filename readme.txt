Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.
Creating a new branch is quick & simple

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
//查看所有分支/当前分支
#git branck (带*为当前分支)

