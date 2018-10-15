## Step1 增加新的分支



 什么是git branch ?  你可以把branch看成一条由每个提交组成的线(时间线),默认的主线名字叫: master.

1.1 查看当前分支git branch

`git branch`{{execute}}



TIPS:

​	当前至少有一个提交,才会产生默认的branch.



1.2 创建一个新的分支dev

`git branch dev`{{execute}}

`git checkout dev`{{execute}}

或者使用'-b'参数,创建并切换至dev分支

`git checkout -b dev`{{execute}}

系统会显示你已经切换到dev分支

```bash
Initialized empty Git repository in /root/myproject/.git/
```



1.3 查看branch

`git branch`{{execute}}

会显示如下信息，表示你当前工作在dev分支

```bash
/myproject # git branch
* dev
  master
/myproject #
```



在下一步,我们会演示如何在分支之间进行工作.