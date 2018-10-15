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

3.2 切换到master分支,(待续)