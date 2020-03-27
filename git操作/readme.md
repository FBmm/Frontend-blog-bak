# Git操作

> 以前对 Git 只是简单使用，今天开始深入学习。

- 参考文章
    - [廖雪峰老师git教程](https://www.liaoxuefeng.com/wiki/896043488029600)

# Git 简介

- 开源
    - Linus 创建了 Linux，后来 Linux 成为最大的开源服务器系统软件
    - Linux代码库日益壮大，无法手工管理，所以 Linus 花两周时间用 C 写了 Git。

- 分布式版本控制系统 Git
    - 每个人的电脑上都有一份完整的版本库
    - 不需要联网
    - 强大的分支管理
    - 个人库和中央仓库一样，服务器挂了可以从任一个个人库拷过去，重新搭建版本库

- 集中式版本控制系统 SVN、CVS
    - 版本库存放在中央服务器
    - 必须联网
    - 每次提交的是 commit
    - 如果服务器挂了，没法恢复，因为个人库没有历史版本库

# Git 安装

- [Git官网下载](https://git-scm.com/downloads)

- 可以选择 Mac、Windows、Linux版本，下载后解压运行即可

配置全局用户名、邮箱，这是你以后提交以及拉取代码的身份信息

``` git
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```

# 创建版本库

- 版本库是代码仓库，仓库可以被 Git 管理起来，以后每个人的提交记录都会被记录。

``` git
mkdir git-test & cd git-test
git init
```


- 提示 'Initialized empty Git repository in D:/_my/git-test/.git/' 表示创建成功
