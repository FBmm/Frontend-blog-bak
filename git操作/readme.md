# git操作
#### 新建代码库
```git
# 在当前目录新建一个Git代码库
git init 

# 新建一个目录，将其初始化为Git代码库
git init [project-name]

#克隆项目和整个history
git clone [url]
```
#### 配置
```git
# 查看当前项目配置
git config --list

# 设置提交代码时的用户信息
git config [--global] user.name "[name]"  // 用户名
git config [--global] user.email "[email address]"  // 邮箱
```
#### 添加暂存文件
```git
# git add之前最好执行git status
#查看当前项目更改状态
# git status

# 暂存所有已更改文件
git add *

# 暂存指定文件
git add [文件名]
git add [文件1] [文件2] ...
 
# 添加当前目录的所有文件到暂存区
$ git add .
```
#### 分支
```git
# 列出所有本地分支
git branch

# 列出所有远端分支
git branch -r

# 新建一个分支，但依然停留在当前分支
git branch [分支名]

# 新建一个分支，并切换到该分支
git checkout -b [分支名]

# 新建切换到该分支，并创建远程分支建立连接
git checkout -b [分支名]
git push origin [分支名]

# 本地分支与远端分支同步并建立关联，没有则新建
git push origin [本地分支名]:[远端分支名]

# 合并目标分支到当前分支
git merge [目标分支名]

# 删除分支
$ git branch -d [分支名]

# 删除远端分支
$ git push origin --delete [分支名]
$ git push origin : [分支名]
```
#### 添加远程仓库
```git
# 为目标远程仓库建立指引(取别名 )
git remote add [别名] [远端仓库url] // git remote add dfv [远端url]  (注：dfv 为别名 表示这个远端地址) 
```
#### 更新代码
```git
# 实际开发中最好每次提交代码前更新代码

# 更新与提交代码前,注意切换分支

# 拉取远端仓库代码，与本地合并
# mater 分支
git pull origin master  // 此处 origin 表示远程仓库地址
# 其他分支
git pull [远端地址\别名] [分支名]  // git pull dfv br_feature
```
#### 代码提交
```git
# 提交暂存区的代码到仓库
git commit -m [注释]

# 提交暂存区的指定文件到仓库区
git commit [文件1] [文件2] ... -m [注释]

# 建议：git commit 后执行 git pull 对比，解决冲突后 git push 推送到远端

# git push
# master分支
git push origin master
# 其他分支
git push dfv br_feature
git push [远程仓库url] [分支名]
```
