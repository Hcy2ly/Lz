<!--
 * @Author: ly
 * @Date: 2020-02-04 23:23:52
 * @LastEditTime : 2020-02-06 23:17:54
 * @LastEditors  : Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \beixiang\LY_Restart\4_Go\readme.md
 -->
# Go
  * Go 是一个开源的编程语言，它能让构造简单、可靠且高效的软件变得容易。
  
  * Go 语言特色
    - 简洁、快速、安全
    - 并行、有趣、开源
    - 内存管理、数组安全、编译迅速
    
  * Go 语言用途
    - Go 语言被设计成一门应用于搭载 Web 服务器，存储集群或类似用途的巨型中央服务器的系统编程语言。
    - 对于高性能分布式系统领域而言，Go 语言无疑比大多数其它语言有着更高的开发效率。它提供了海量并行的支持，这对于游戏服务端的开发而言是再好不过了。

  * 计算机软件经历了数十年的发展，形成了多种学术流派，有面向过程编程、面向对象编程、函数式编程、面向消息编程等，这些思想究竟孰优孰劣，众说纷纭。除了OOP外，近年出现了一些小众的编程哲学，Go语言对这些思想亦有所吸收。例如，Go语言接受了函数式编程的一些想法，支持匿名函数与闭包。再如，Go语言接受了以Erlang语言为代表的面向消息编程思想，支持goroutine和通道，并推荐使用消息而不是共享内存来进行并发编程。总体来说，Go语言是一个非常现代化的语言，精小但非常强大。

  * Go 语言最主要的特性：
    - 自动垃圾回收
    - 更丰富的内置类型
    - 函数多返回值
    - 错误处理
    - 匿名函数和闭包
    - 类型和接口
    - 并发编程
    - 反射
    - 语言交互性
    - LeonWilliam

# Go语言基础语法
  * 关键字
    下面列举了 Go 代码中会使用到的 25 个关键字或保留字：

    break	default	func	interface	select
    case	defer	go	map	struct
    chan	else	goto	package	switch
    const	fallthrough	if	range	type
    continue	for	import	return	var
    除了以上介绍的这些关键字，Go 语言还有 36 个预定义标识符：

    append	bool	byte	cap	close	complex	complex64	complex128	uint16
    copy	false	float32	float64	imag	int	int8	int16	uint32
    int32	int64	iota	len	make	new	nil	panic	uint64
    print	println	real	recover	string	true	uint	uint8	uintptr
    程序一般由关键字、常量、变量、运算符、类型和函数组成。

    程序中可能会使用到这些分隔符：括号 ()，中括号 [] 和大括号 {}。

    程序中可能会使用到这些标点符号：.、,、;、: 和 …。
    
  * 字符串连接
      Go 语言的字符串可以通过 + 实现：
  
  * Go 语言的空格
      Go 语言中变量的声明必须使用空格隔开，如：var age int;

# Go 语言数据类型
在 Go 编程语言中，数据类型用于声明函数和变量。
数据类型的出现是为了把数据分成所需内存大小不同的数据，编程的时候需要用大数据的时候才需要申请大内存，就可以充分利用内存。
  * Go 语言按类别有以下几种数据类型：
    序号	类型和描述
    1	布尔型
    布尔型的值只可以是常量 true 或者 false。一个简单的例子：var b bool = true。
    2	数字类型
    整型 int 和浮点型 float32、float64，Go 语言支持整型和浮点型数字，并且支持复数，其中位的运算采用补码。
    3	字符串类型:
    字符串就是一串固定长度的字符连接起来的字符序列。Go 的字符串是由单个字节连接起来的。Go 语言的字符串的字节使用 UTF-8 编码标识 Unicode 文本。
    4	派生类型:
    包括：
    (a) 指针类型（Pointer）
    (b) 数组类型
    (c) 结构化类型(struct)
    (d) Channel 类型
    (e) 函数类型
    (f) 切片类型
    (g) 接口类型（interface）
    (h) Map 类型
      
  * 数字类型
  Go 也有基于架构的类型，例如：int、uint 和 uintptr。
    序号	类型和描述
    1	uint8
    无符号 8 位整型 (0 到 255)
    2	uint16
    无符号 16 位整型 (0 到 65535)
    3	uint32
    无符号 32 位整型 (0 到 4294967295)
    4	uint64
    无符号 64 位整型 (0 到 18446744073709551615)
    5	int8
    有符号 8 位整型 (-128 到 127)
    6	int16
    有符号 16 位整型 (-32768 到 32767)
    7	int32
    有符号 32 位整型 (-2147483648 到 2147483647)
    8	int64
    有符号 64 位整型 (-9223372036854775808 到 9223372036854775807)
    
  * 浮点型
    序号	类型和描述
    1	float32
    IEEE-754 32位浮点型数
    2	float64
    IEEE-754 64位浮点型数
    3	complex64
    32 位实数和虚数
    4	complex128
    64 位实数和虚数

  * 其他数字类型
以下列出了其他更多的数字类型：
  序号	类型和描述
  1	byte
  类似 uint8
  2	rune
  类似 int32
  3	uint
  32 或 64 位
  4	int
  与 uint 一样大小
  5	uintptr
  无符号整型，用于存放一个指针

# Go 语言变量
  1. 数值类型（包括complex64/128）为 0

  2. 布尔类型为 false

  3. 字符串为 ""（空字符串）

  4. 以下几种类型为 nil：
    var a *int
    var a []int
    var a map[string] int 
    var a chan int
    var a func(string) int
    var a error // error 是接口

# Go 语言常量
常量是一个简单值的标识符，在程序运行时，不会被修改的量。
常量中的数据类型只可以是布尔型、数字型（整数型、浮点型和复数）和字符串型。

* 常量的定义格式：const identifier [type] = value

* 你可以省略类型说明符 [type]，因为编译器可以根据变量的值来推断其类型。
  显式类型定义： const b string = "abc"
  隐式类型定义： const b = "abc"

* 多个相同类型的声明可以简写为：const c_name1, c_name2 = value1, value2

* 常量还可以用作枚举：数字 0、1 和 2 分别代表未知性别、女性和男性。
    const (
        Unknown = 0
        Female = 1
        Male = 2
    )
    
* iota，特殊常量，可以认为是一个可以被编译器修改的常量。
iota 在 const关键字出现时将被重置为 0(const 内部的第一行之前)，const 中每新增一行常量声明将使 iota 计数一次(iota 可理解为 const 语句块中的行索引)。
iota 可以被用作枚举值：
  const (
      a = iota
      b = iota
      c = iota
  )

* 再看个有趣的的 iota 实例：
    const (
        i=1<<iota  // iota = 0
        j=3<<iota  // iota++ 1
        k  // k=3<< iota++ 2
        l  // l=3<< iota++ 3
    )

    func main() {
        fmt.Println("i=",i)
        fmt.Println("j=",j)
        fmt.Println("k=",k)
        fmt.Println("l=",l)
    }
    以上实例运行结果为：

    i= 1
    j= 6
    k= 12
    l= 24
    iota 表示从 0 开始自动加 1，所以 i=1<<0, j=3<<1（<< 表示左移的意思），即：i=1, j=6，这没问题，关键在 k 和 l，从输出结果看 k=3<<2，l=3<<3。

    简单表述:
      i=1：左移 0 位,不变仍为 1;  //1二进制0001 左移0位0001 还是 2^0*1 = 1
      j=3：左移 1 位,变为二进制 110, 即 6;  //3二进制0011 左移1位为0110 换成十进制为 2^0*0 + 2^1*1 + 2^2*1  = 0+2+4 = 6
      k=3：左移 2 位,变为二进制 1100, 即 12;  //3二进制0011 左移2位为1100 换成十进制为 2^0*0 + 2^1*0 + 2^2*1 + 2^3*1 = 4+8 = 12
      l=3：左移 3 位,变为二进制 11000,即 24。 //3二进制0011 左移3位为11000 换成十进制为 2^0*0 + 2^1*0 + 2^2*0 + 2^3*1 + 2^4*1= 8+16 = 24

# Go 语言运算符
运算符用于在程序运行时执行数学或逻辑运算。
  * Go 语言内置的运算符有：
    算术运算符
    关系运算符
    逻辑运算符
    位运算符
    赋值运算符
    其他运算符

    - 算术运算符
    下表列出了所有Go语言的算术运算符。假定 A 值为 10，B 值为 20。
      运算符	描述	实例
      +	相加	A + B 输出结果 30
      -	相减	A - B 输出结果 -10
      *	相乘	A * B 输出结果 200
      /	相除	B / A 输出结果 2
      %	求余	B % A 输出结果 0
      ++	自增	A++ 输出结果 11
      --	自减	A-- 输出结果 9

    - 关系运算符
    下表列出了所有Go语言的关系运算符。假定 A 值为 10，B 值为 20。
      运算符	描述	实例
      ==	检查两个值是否相等，如果相等返回 True 否则返回 False。	(A == B) 为 False
      !=	检查两个值是否不相等，如果不相等返回 True 否则返回 False。	(A != B) 为 True
      >	检查左边值是否大于右边值，如果是返回 True 否则返回 False。	(A > B) 为 False
      <	检查左边值是否小于右边值，如果是返回 True 否则返回 False。	(A < B) 为 True
      >=	检查左边值是否大于等于右边值，如果是返回 True 否则返回 False。	(A >= B) 为 False
      <=	检查左边值是否小于等于右边值，如果是返回 True 否则返回 False。	(A <= B) 为 True

    - 逻辑运算符
    下表列出了所有Go语言的逻辑运算符。假定 A 值为 True，B 值为 False。
      运算符	描述	实例
      &&	逻辑 AND 运算符。 如果两边的操作数都是 True，则条件 True，否则为 False。	(A && B) 为 False
      ||	逻辑 OR 运算符。 如果两边的操作数有一个 True，则条件 True，否则为 False。	(A || B) 为 True
      !	逻辑 NOT 运算符。 如果条件为 True，则逻辑 NOT 条件 False，否则为 True。	!(A && B) 为 True

    - 位运算符
    位运算符对整数在内存中的二进制位进行操作。
    下表列出了位运算符 &, |, 和 ^ 的计算：
      p	q	p & q	p | q	p ^ q
      0	0	0	0	0
      0	1	0	1	1
      1	1	1	1	0
      1	0	0	1	1
      
      假定 A = 60; B = 13; 其二进制数转换为：
      A = 0011 1100
      B = 0000 1101
      -----------------
      A&B = 0000 1100
      A|B = 0011 1101
      A^B = 0011 0001

      Go 语言支持的位运算符如下表所示。假定 A 为60，B 为13：
        运算符	描述	实例
        &	按位与运算符"&"是双目运算符。 其功能是参与运算的两数各对应的二进位相与。	(A & B) 结果为 12, 二进制为 0000 1100
        |	按位或运算符"|"是双目运算符。 其功能是参与运算的两数各对应的二进位相或	(A | B) 结果为 61, 二进制为 0011 1101
        ^	按位异或运算符"^"是双目运算符。 其功能是参与运算的两数各对应的二进位相异或，当两对应的二进位相异时，结果为1。	(A ^ B) 结果为 49, 二进制为 0011 0001
        <<	左移运算符"<<"是双目运算符。左移n位就是乘以2的n次方。 其功能把"<<"左边的运算数的各二进位全部左移若干位，由"<<"右边的数指定移动的位数，高位丢弃，低位补0。	A << 2 结果为 240 ，二进制为 1111 0000
        >>	右移运算符">>"是双目运算符。右移n位就是除以2的n次方。 其功能是把">>"左边的运算数的各二进位全部右移若干位，">>"右边的数指定移动的位数。	A >> 2 结果为 15 ，二进制为 0000 1111

    - 赋值运算符
    下表列出了所有Go语言的赋值运算符。
      运算符	描述	实例
      =	简单的赋值运算符，将一个表达式的值赋给一个左值	C = A + B 将 A + B 表达式结果赋值给 C
      +=	相加后再赋值	C += A 等于 C = C + A
      -=	相减后再赋值	C -= A 等于 C = C - A
      *=	相乘后再赋值	C *= A 等于 C = C * A
      /=	相除后再赋值	C /= A 等于 C = C / A
      %=	求余后再赋值	C %= A 等于 C = C % A
      <<=	左移后赋值	C <<= 2 等于 C = C << 2
      >>=	右移后赋值	C >>= 2 等于 C = C >> 2
      &=	按位与后赋值	C &= 2 等于 C = C & 2
      ^=	按位异或后赋值	C ^= 2 等于 C = C ^ 2
      |=	按位或后赋值	C |= 2 等于 C = C | 2

    - 其他运算符
下表列出了Go语言的其他运算符。
  运算符	描述	实例
  &：	返回变量存储地址	&a; 将给出变量的实际地址。
  *： 指针变量。	*a; 是一个指针变量

  * 运算符优先级
  有些运算符拥有较高的优先级，二元运算符的运算方向均是从左至右。下表列出了所有运算符以及它们的优先级，由上至下代表优先级由高到低：
    优先级	运算符
    5	* / % << >> & &^
    4	+ - | ^
    3	== != < <= > >=
    2	&&
    1	||
    当然，你可以通过使用括号来临时提升某个表达式的整体运算优先级。

    

# Go 语言条件语句
  * Go 语言提供了以下几种条件判断语句：
    语句	描述
    if 语句	if 语句 由一个布尔表达式后紧跟一个或多个语句组成。
    if...else 语句	if 语句 后可以使用可选的 else 语句, else 语句中的表达式在布尔表达式为 false 时执行。
    if 嵌套语句	你可以在 if 或 else if 语句中嵌入一个或多个 if 或 else if 语句。
    switch 语句	switch 语句用于基于不同条件执行不同动作。
    select 语句	select 语句类似于 switch 语句，但是select会随机执行一个可运行的case。如果没有case可运行，它将阻塞，直到有case可运行。
    
  * 注意：Go 没有三目运算符，所以不支持 ?: 形式的条件判断。


# Go 语言循环语句

  * Go 语言提供了以下几种类型循环处理语句：
    循环类型	描述
    for 循环	重复执行语句块
    循环嵌套	在 for 循环中嵌套一个或多个 for 循环

  * 循环控制语句
    循环控制语句可以控制循环体内语句的执行过程。
    GO 语言支持以下几种循环控制语句：
      控制语句	描述
      break 语句	经常用于中断当前 for 循环或跳出 switch 语句
      continue 语句	跳过当前循环的剩余语句，然后继续进行下一轮循环。
      goto 语句	将控制转移到被标记的语句。
      for无限循环：
        func main() {
          for true  {
              fmt.Printf("这是无限循环。\n");
          }
        }

# Go 语言函数
  * 
  func function_name( [parameter list] ) [return_types] {
    函数体
  }
  函数定义解析：
    func：函数由 func 开始声明
    function_name：函数名称，函数名和参数列表一起构成了函数签名。
    parameter list：参数列表，参数就像一个占位符，当函数被调用时，你可以将值传递给参数，这个值被称为实际参数。参数列表指定的是参数类型、顺序、及参数个数。参数是可选的，也就是说函数也可以不包含参数。
    return_types：返回类型，函数返回一列值。return_types 是该列值的数据类型。有些功能不需要返回值，这种情况下 return_types 不是必须的。
    函数体：函数定义的代码集合。
  * 函数参数
   - 函数如果使用参数，该变量可称为函数的形参。
   - 形参就像定义在函数体内的局部变量。
   - 调用函数，可以通过两种方式来传递参数：
      传递类型	描述
      值传递	值传递是指在调用函数时将实际参数复制一份传递到函数中，这样在函数中如果对参数进行修改，将不会影响到实际参数。
      引用传递	引用传递是指在调用函数时将实际参数的地址传递到函数中，那么在函数中对参数所进行的修改，将影响到实际参数。
   * 默认情况下，Go 语言使用的是值传递，即在调用过程中不会影响到实际参数。

  * 函数用法
    函数用法	描述
    函数作为另外一个函数的实参	函数定义后可作为另外一个函数的实参数传入
    闭包	闭包是匿名函数，可在动态编程中使用
    方法	方法就是一个包含了接受者的函数 

# Go语言变量作用域
  * 作用域为已声明标识符所表示的常量、类型、变量、函数或包在源代码中的作用范围。

  * Go 语言中变量可以在三个地方声明：
      - 函数内定义的变量称为局部变量
      - 函数外定义的变量称为全局变量
      - 函数定义中的变量称为形式参数

  * 局部变量
  在函数体内声明的变量称之为局部变量，它们的作用域只在函数体内，参数和返回值变量也是局部变量。

  * 全局变量
  在函数体外声明的变量称之为全局变量，全局变量可以在整个包甚至外部包（被导出后）使用。
  全局变量可以在任何函数中使用。

  * ps： Go 语言程序中全局变量与局部变量名称可以相同，但是函数内的局部变量会被优先考虑

  * 形式参数 形式参数会作为函数的局部变量来使用。

  * 初始化局部和全局变量
    不同类型的局部和全局变量默认值为：
      数据类型	初始化默认值
      int	0
      float32	0
      pointer	nil

# Go 语言数组
Go 语言提供了数组类型的数据结构。
数组是具有相同唯一类型的一组已编号且长度固定的数据项序列，这种类型可以是任意的原始类型例如整形、字符串或者自定义类型。
相对于去声明 number0, number1, ..., number99 的变量，使用数组形式 numbers[0], numbers[1] ..., numbers[99] 更加方便且易于扩展。
数组元素可以通过索引（位置）来读取（或者修改），索引从 0 开始，第一个元素索引为 0，第二个索引为 1，以此类推。
  * 声明数组
  Go 语言数组声明需要指定元素类型及元素个数，语法格式如下：var variable_name [SIZE] variable_type

    - 以上为一维数组的定义方式。例如以下定义了数组 balance 长度为 10 类型为   float32：var balance [10] float32

  * 初始化数组
   - 以下演示了数组初始化：var balance = [5]float32{1000.0, 2.0, 3.4, 7.0, 50.0}
    ps：初始化数组中 {} 中的元素个数不能大于 [] 中的数字。

   - 如果忽略 [] 中的数字不设置数组大小，Go 语言会根据元素的个数来设置数组的大小： var balance = [...]float32{1000.0, 2.0, 3.4, 7.0, 50.0}
   ps: balance[4] = 50.0 // 读取了第五个元素。

  * 访问数组元素
  数组元素可以通过索引（位置）来读取。格式为数组名后加中括号，中括号为索引的值。
  eg: var salary float32 = balance[9] // 读取了数组的第10个元素的值。
    - 数组对 Go 语言来说是非常重要的，以下我们将介绍数组更多的内容：
      内容	描述
      多维数组	Go 语言支持多维数组，最简单的多维数组是二维数组
      向函数传递数组	你可以向函数传递数组参数
      
  * 初始化数组的初始化有多种形式。
    1. [5] int {1,2,3,4,5}
    长度为5的数组，其元素值依次为：1，2，3，4，5。

    2. [5] int {1,2}
    长度为 5 的数组，其元素值依次为：1，2，0，0，0 。
    在初始化时没有指定初值的元素将会赋值为其元素类型 int 的默认值0，string 的默认值是 ""。

    3. [...] int {1,2,3,4,5}
    长度为 5 的数组，其长度是根据初始化时指定的元素个数决定的。

    4. [5] int { 2:1,3:2,4:3}
    长度为 5 的数组，key:value，其元素值依次为：0，0，1，2，3。在初始化时指定了 2，3，4 索引中对应的值：1，2，3

    5. [...] int {2:1,4:3}
    长度为5的数组，起元素值依次为：0，0，1，0，3。由于指定了最大索引 4 对应的值 3，根据初始化的元素个 数确定其长度为5赋值与使用。

    6. 切片的初始化
    切片可以通过数组来初始化，也可以通过内置函数 make() 初始化。
    初始化时 len=cap，在追加元素时如果容量 cap 不足时将按 len 的 2 倍扩容。

    s :=[] int {1,2,3 } 直接初始化切片，[] 表示是切片类型，{1,2,3} 初始化值依次是 1,2,3。其 cap=len=3。

    s := arr[:] 初始化切片 s，是数组 arr 的引用。

    s := arr[startIndex:endIndex] 将 arr 中从下标 startIndex 到 endIndex-1 下的元素创建为一个新的切片。

    s := arr[startIndex:] 缺省 endIndex 时将表示一直到 arr 的最后一个元素。

    s := arr[:endIndex] 缺省 startIndex 时将表示从 arr 的第一个元素开始。

    s1 := s[startIndex:endIndex] 通过切片 s 初始化切片 s1

    s :=make([]int,len,cap) 通过内置函数 make() 初始化切片 s,[]int 标识为其元素类型为 int 的切片。

   