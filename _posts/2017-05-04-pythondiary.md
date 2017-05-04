### Python日记 2017-05-04 傍晚
#### 高阶函数

**1**. 变量可以指向函数
```
def calc(x):
    return x**x
f=calc
print(f(2))
>>> 4
```
函数式编程还是比较有意思的:
>函数是Python内建支持的一种封装，我们通过把大段代码拆成函数，通过一层一层的函数调用，就可以把复杂任务分解成简单的任务，这种分解可以称之为面向过程的程序设计。函数就是面向过程的程序设计的基本单元。
而函数式编程（请注意多了一个“式”字）——Functional Programming，虽然也可以归结到面向过程的程序设计，但其思想更接近数学计算。
我们首先要搞明白计算机（Computer）和计算（Compute）的概念。
在计算机的层次上，CPU执行的是加减乘除的指令代码，以及各种条件判断和跳转指令，所以，汇编语言是最贴近计算机的语言。
而计算则指数学意义上的计算，越是抽象的计算，离计算机硬件越远。
对应到编程语言，就是越低级的语言，越贴近计算机，抽象程度低，执行效率高，比如C语言；越高级的语言，越贴近计算，抽象程度高，执行效率低，比如Lisp语言。
函数式编程就是一种抽象程度很高的编程范式，纯粹的函数式编程语言编写的函数没有变量，因此，任意一个函数，只要输入是确定的，输出就是确定的，这种纯函数我们称之为没有副作用。而允许使用变量的程序设计语言，由于函数内部的变量状态不确定，同样的输入，可能得到不同的输出，因此，这种函数是有副作用的。
函数式编程的一个特点就是，允许把函数本身作为参数传入另一个函数，还允许返回一个函数！
Python对函数式编程提供部分支持。由于Python允许使用变量，因此，Python不是纯函数式编程语言。

**2**. map()函数接收两个参数，一个是函数，一个是Iterable(迭代)，map将传入的函数依次作用到序列的每个元素，并把结果作为新的Iterator返回。
看map函数的几段实用代码:
```
list(map(str, [1, 2, 3, 4, 5, 6, 7, 8, 9]))
#把列表中的数字转为字符串
```
#### 切片
```
age_list=[1,2,3,4,5,6]
name="alexs"
print age_list[:3]
print (name[2:4])
>>> [1,2,3]
>>> "ex"
```
#### 迭代
**1.** Python dict类型默认迭代对象是key，示例：
```
name_dict={"age":10,"name":"alexs","engine":["google","baidu"]}
for key in name_dict:
      print (key)
```
**2.** 如果要迭代value，可以这样：
```
name_dict={"age":10,"name":"alexs","engine":["google","baidu"]}
for value in name_dict.values():
      print (value)
```
**3.** 如果同时迭代key和value，可以这样：
```
name_dict={"age":10,"name":"alexs","engine":["google","baidu"]}
for key,value in name_dict.items():
      print (key,value)
```
**4.** 在Python中可以把字符串看成有list属性的string，可以这样：
```
name="wulamier_alexs"
for i in name:
      print (i)
```
**5.** 对list进行key-value方式迭代：
```
name_list=["sun","ibm","Google","Bing"]
for n,i in enumerate(name_list):
      print (n,i)
```
