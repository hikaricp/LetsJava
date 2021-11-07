Java基础数据类型

!!! quote
    “In Go, the code does exactly what it says on the page.” – Andrew Gerrand

* int
* short
* byte
* long
* char
* boolean
* float
* double



**我是你爸爸**

```java
public static void main(String[] args) {
  System.out.println("Hello World");
}
```

## 静态/动态类型，弱类型/强类型

静态，动态类型指的是类型是在编译期还是运行期间确定，而弱类型和强类型指的是有没有隐式类型转换。
比如 Python 就是动态强类型语言(很多人误以为弱类型)，而 php/js 是动态弱类型语言。
go 是静态强类型语言，我们在编写代码的时候需要先声明变量的类型（或者编译器推导），
在不同类型之间转换的时候需要我们强制使用类型转换符。

## go 如何声明一个变量

go 中声明一个变量很简单，使用 var 关键字就可以了，声明之后默认使用其类型的零值初始化。
比如int 类型默认是0，字符串就是空串。

当然为了简化 go 还提供了一种使用 `:=` 直接声明并且初始化的方式。请编写如下代码观察输出(我建议你纯手敲练练手速，不要直接复制)：

```go
package main

import "fmt"

func main() {
	var i int64             // 声明一个 int64 变量。注意类型放在后边，习惯就好了
	var b string            // 声明一个字符串
	fmt.Println("i is ", i) // 0
	fmt.Println("b is ", b) // ""

	// 同时声明并且赋值
	var floatNum float64 = 1.0
	var price1, price2 float64 = 8.8, 9.6
	fmt.Println(floatNum, price1, price2)

	// 还有一种简化方式，声明并且赋值，编译器负责推断类型
	ii := 1
	s := "Hello Go!"
	fmt.Println("ii is ", ii) // 1
	fmt.Println("s is ", s)   // Hello Go!"
}
```

## Go 的基础类型

无论是学习过程式、面向对象还是并发编程，我们都需要首先学习一门语言的基础类型，对于大部分业务常用编程语言来说就是数值类型和字符串类型。

### bool 类型

bool 就是真或者假，一些编程语言使用 0 和非 0 表示。但是 go 里比如 if 语句后边只能是 bool 值或者返回 bool
值的表达式，而不像 c 一样可以使用 int 值。



| 姓名   | 性别 | 身份证号           |
| ------ | ---- | ------------------ |
| 杨佳畅 | 男   | 123456789          |
| 詹姆斯 | 男   | 2432432423423      |
| 科比   | 男   | 诶是的范德萨发生的 |

