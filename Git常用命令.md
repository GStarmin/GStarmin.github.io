# Git常用命令

## 修改之后提交的流程
```
git add .
git commit -m "注释内容"  
git push   
git push origin main
```
## Git连接远程仓库

`git remote add origin url`


注：url为github仓库链接

## Git删除已经add的文件
1.要删除的文件少时

一种是 `git rm --cached` “文件路径”，不删除物理文件，仅将该文件从缓存中删除；
一种是 `git rm --f` “文件路径”，不仅将该文件从缓存中删除，还会将物理文件删除（不会回收到垃圾桶）。

2.要删除的文件多时

`git rm -r --cached` . 清空缓存区
然后将本地文件删除，再次add

## Git撤销commit命令
当要撤销的提交不是最开始的提交时  
`git reset HEAD~ ` 
当要撤销的提交时最开始的提交时  
`git update-ref -d HEAD`

## Git创建远程新分支
git无法直接通过命令方式创建远程新分支，需要间接来创建  
这里我创建的远程新分支名叫 vedio  
首先 `git checkout --orphan 分支名`  
![checkout到分支名](./pic/Git常用命令/Git创建远程分支.png)  
`git rm -rf .` （这一步很关键）

然后创建一个文件readme.md（其实任何文件都可以），add并commit，然后git push origin 分支名 就可以啦~
如下图红框圈注的命令  
![红圈注释](./pic/Git常用命令/pic1.png)

## git强制提交本地分支覆盖远程分支
`git push origin main --force`
或
`git push origin main -f`

## Git从远程仓库拉取
`git pull origin main`

## Git创建与切换分支
- 创建分支 `git branch branch_name ` 
- 切换分支 `git checkout branch_name`