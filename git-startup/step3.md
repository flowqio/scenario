## Step3 如何忽略某类文件

3.1 如何忽略某类文件

在代码仓库里可能有某些静态资源文件比如图片,二进制文件不想放入代码仓库跟踪,可以通过编辑.gitignore 文件实现

`echo ".gitignore" > .gitignore` {{execute}}

` echo "static/" > .gitignore`{{execute}}

通过上面2条命令,我们建立了.gitignore文件,并且让git自动忽略了.gitignore文件和static目录

这样static目录下面所有的文件都不会被git跟踪.

到此为止,我们完成了一个代码仓库的初始化、添加文件、忽略某类/某个目录的文件.