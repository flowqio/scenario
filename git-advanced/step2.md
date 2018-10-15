## Step2 在master与dev之间进行提交

2.1 首先我们回到master

`git checkout master`{{execute}}

`vi main.go`{{execute}}

我们编辑一个main.go

```go
package main

import (
    "fmt"
)


func main(){
        fmt.Println("hello golang")
}
```



然后进行提交

`git add main.go`{{execute}}

`git commit -m "add main.go"`{{execute}}



2.2 切换到dev分支

现在我们可以切换到dev分支创建新的函数Add

`mkdir -p src/add`{{execute}}

`vi src/add/add.go`{{execute}}

```go
package add

func Add(x,y int) int{
    return x+y
}
```

`git add src/add/add.go`{{execute}}

`git commit -m "add Add"`{{execute}}

这个时候我们就完成了在dev分支下面Add函数的开发.

 

2.3  切换回到master分支

`git checkout master`{{execute}}

然后我们执行关键的一步,将dev分支的add.go合并到master分支上

`git merge dev`{{execute}}



2.4  查看提交日志

`git log`


到此为止我们完成了在master于dev之间的切换,并且把dev的修改合并到master分支上