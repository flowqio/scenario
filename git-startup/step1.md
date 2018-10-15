## Step1 初始化代码仓库:



1.1 查看git 是否可以正常工作

`git`{{execute}}

如果已经安装了, 该命令会返回git所有的参数

1.2 初始化一个代码仓库目录(myproject)

`mkdir myproject `{{execute}}

`cd  myproject `{{execute}}

`git init `{{execute}}

系统会显示初成功始化仓库

```bash
Initialized empty Git repository in /root/myproject/.git/
```



1.3 查看状态

`git status`{{execute}}

会显示如下信息，表示目前没有任何提交(commit)

```bash
~/myproject #  git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
```



在下一步,我们会提交一个README.md 文件.