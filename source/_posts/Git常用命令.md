---
title: Git常用命令
math: true
---


## Git撤销commit命令
当要撤销的提交不是最开始的提交时
```
git reset HEAD~
```
当要撤销的提交时最开始的提交时
```
git update -ref -d HEAD
```
## Git连接远程仓库
```
git remote add origin url
```
注：url为github仓库链接
## Git删除已经add的文件
1.要删除的文件少时
	一种是 `git rm --cached` "文件路径"，不删除物理文件，仅将该文件从缓存中删除；
	一种是 `git rm --f`  "文件路径"，不仅将该文件从缓存中删除，还会将物理文件删除（不会回收到垃圾桶）。


2.要删除的文件多时
	`git rm -r --cached` .  清空缓存区
	然后将本地文件删除，再次`add`
	

## Git创建远程新分支
git无法直接通过命令方式创建远程新分支，需要间接来创建,这里我创建的远程新分支名叫 vedio


首先 

`git checkout --orphan 分支名`
![](https://img-blog.csdnimg.cn/20210403164118752.png)
**git rm -rf .** （这一步很关键）
然后创建一个文件readme.md（其实任何文件都可以），add并commit，然后

`git push origin 分支名` 

就可以啦~如下图红框圈注的命令
![](https://img-blog.csdnimg.cn/20210403164816128.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzkzOTQyMQ==,size_16,color_FFFFFF,t_70)
## git强制提交本地分支覆盖远程分支
```
git push origin localBranchName:remoteBranchName --force
```
## Git从远程仓库拉取
`git pull origin main`
## Git创建与切换分支
创建分支 `git branch branch_name`
切换分支 `git checkout branch_name`








