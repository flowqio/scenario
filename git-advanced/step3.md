## Step3 如何解决合并中的冲突

在Step2中我们创建的dev分支,并且将它的改动合并到master分支中,下面我们就来看看如何解决合并中产生的冲突。

3.1 切换到dev分支,创建一个有冲突的提交

`git checkout dev`{{execute}}

`vi main.go`{{execute}}

很简单我们修改main.go,我们增加了一个log.Println的调用

```go
package main

import (
    "log"
    "fmt"
)

func main(){
    log.Println("dev version")        
    fmt.Println("hello golang")
}
```



`git add main.go`{{execute}}

`git commit -m "update main.go /dev branch"`{{execute}}

在Step2中我们创建的dev分支,并且将它的改动合并到master分支， 但是我们这次实在dev分支下面修改了main.go这样在合并的时候就会产生冲突.

3.2 切换到master分支

`git checkout master`{{execute}}

`git merge dev` {{execute}}

注意现在git提供了一个Fast-Forward模式，尽量坚持冲突的发生

如果你希望看见上面的修改出现冲突请使用 `git merge --no-ff dev` {{execute}} ,'--no-ff'参数会让git禁止Fast-Foward 特性

```bash
#Fast-forward
/myproject # git merge dev
Updating 11b88f2..9b5ffbe
Fast-forward
 main.go | 1 -
 1 file changed, 1 deletion(-)


#Disable Fast-forward 模式
/myproject # git merge --no-ff dev
Auto-merging main.go
CONFLICT (content): Merge conflict in main.go
Automatic merge failed; fix conflicts and then commit the result.
/myproject # cat main.go
package main

import (
    "log"
    "fmt"
)

func main(){
    log.Println("dev update version")
<<<<<<< HEAD
    fmt.Println("add comment master  agaion")
=======
    fmt.Println("add comment dev1 agaion")
>>>>>>> dev
}


func other(){
    //this comments
}
/myproject #

#修改冲突之后提交重新merge就好了
/myproject # git add main.go
/myproject # git merge --no-ff dev
fatal: You have not concluded your merge (MERGE_HEAD exists).
Please, commit your changes before you merge.
/myproject # git commit -m "master update"
[master 70f0b06] master update
/myproject # git merge --no-ff dev
Already up to date.
/myproject #
```

