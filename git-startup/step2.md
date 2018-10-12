## Step2 提交一个README

2.1 配置邮箱和用户名

这里我们使用全局方式配置git的用户名,邮箱.

```bash
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```



2.2 编辑一个README

我们在Step1 创建了一个myproject的目录，并且已经完成初始化了，现在我们准备提交一个README文件

`echo "# myproject" > README`{{execute}}

`git status`{{execute}}

git 会自动发现当前目录有文件变化(Untracked file),提示我们进行提交.

 

2.3  添加并提交

这个是2步，第一步通过git add 添加, 第二步通过git commit 提交。

`git add README`{{execute}}

`git commit -m "add README"`



会显示如下信息

```bash
[master (root-commit) aab995c] add README.md
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
```



TIPS:

   如果你想要一步完成提交当前所有改动文件可以使用 git commit -a -m "<message>"



2.3 查看提交日志

`git log`


到此为止我们完成了README的本地提交