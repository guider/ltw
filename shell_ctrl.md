## SHELL 中常用的`Ctrl`操作
* `Ctrl + c` 发送信号: SIGINT。强制中断
* `Ctrl + z` 发送信号: SIGSTOP。将任务放到后台执行，可以使用fg/bg/jobs操作
* `Ctrl + d` 发送特殊的二进制，表示EOF
在脚本中可以使用`echo -e '\001'`或者`echo $'0032'`实现`Ctrl + a`或`Ctrl + z`<br>
* `Ctrl + s` shell 锁屏
* `Ctrl + q` shell 解锁
