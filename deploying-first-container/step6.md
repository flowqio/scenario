## Step6 在前台运行container

Jack已经成功使用docker run 在后台运行了Redis服务, 同时他还想在前台运行container,比如运行一个bash或者ps.

之前Jack通过使用 -d 设置container在后台运行,如果Jack想运行交互式的程序 可以通过-it实现.

任务

Jack尝试着使用docker run 前台运行ubuntu的 /bin/bash

`docker run -it ubuntu bash`{{execute}} 


扩展练习

如果使用了docker run -it 前台运行了container,当你退出的时候该container也会退出,如果想在已经运行的container上运行一个新的命令(比如ps)可以通过docker exec ,在其他课程里面我们会详细阐述docker run 和docker exec的区别。