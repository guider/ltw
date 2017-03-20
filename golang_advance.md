* 00.断言(assertion)
	* 00.通过`.`符号实现
	* 01.通过`_`符号实现
* 01.不定参数
	* 00.传入数组示例:
```golang
package main

import "fmt"

func show(args ...int){
	for _, v := range args {
        fmt.Println(v)
    
	}

}

func main() {
    slice:=[]int{1,2,3,4}
    show(slice...)

}
```

* 02.代码块
	* 00.使用`{}`符号
* 03.跳转
	* 00.`goto`
	* 01.`continue`
	* 02.`break`
* 04.匿名函数
	* 匿名函数示例:
```golang
package main

import "fmt"

var a int = func() (b int) {
	fmt.Printf("%d\n", b)
	return 1

}()

func main() {
	fmt.Printf("result is %d\n", a)

}

```

* 05.for 调试
```golang
var _ = fmt.Println //for debugger
```
*避免开发时使用 fmt，发布时去掉调试信息提示 fmt 包引入没使用*
