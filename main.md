# Python基础教程
传送门[【GitHub/Icingworld】](https://github.com/Icingworld/python-course-series/)  
2021-7-21 v1.0 by 蒋梓文
* * *
## 目录
+ 引言
+ 一、什么是Python
  + 1.1 python介绍
  + 1.2 python语法
+ 二、Python的变量、类型及运算
  + 2.1 变量的定义
  + 2.2 变量的类型
  + 2.3 运算符
    + 2.3.1 算术运算符
    + 2.3.2 比较运算符
    + 2.3.3 赋值运算符
    + 2.3.4 逻辑运算符
    + 2.3.5 位运算符
    + 2.3.6 成员运算符
    + 2.3.7 身份运算符
    + 2.3.8 运算符优先级（略）
  + 2.4 字符串
    + 2.4.1 字符串访问
    + 2.4.2 字符串拼接
    + 2.4.3 字符串运算
    + 2.4.4 常用内置函数
  + 2.5 列表
    + 2.5.1 列表访问、拼接、运算
    + 2.5.2 常用内置函数
  + 2.6 元组
    + 2.6.1 元组的特殊性质
    + 2.6.2 元组访问、拼接、运算
  + 2.7 字典
    + 2.7.1 字典定义
    + 2.7.2 字典值访问
    + 2.7.3 字典修改
    + 2.7.4 字典删除
    + 2.7.5 字典特性
+ 三、标识符及关键字
+ 四、Python输入输出
  + 4.1 输入
  + 4.2 输出
    + 4.2.1 普通输出
    + 4.2.2 格式化输出
+ 五、条件语句和循环语句
  + 5.1 if
  + 5.2 while
  + 5.3 for
  + 5.4 break、continue和pass
    + 5.4.1 break
    + 5.4.2 continue
    + 5.4.3 pass
+ 六、函数
  + 6.1 函数定义
  + 6.2 函数调用
  + 6.3 参数传递
  + 6.4 参数类型（略）
  + 6.5 作用域
+ 七、模块导入
+ 八、文件I/O
  + 8.1 `open()`方法
  + 8.2 文件操作模式
  + 8.3 使用方法
+ 九、异常抛出
  + 9.1 结构
  + 9.2 常见异常
+ 十、Python基础挑战题！
+ 十一、学习网站
+ 十二、总结
* * *
## 引言
本教程适用于无基础急需入门小白，看完本文即可上手python基础应用  
后续会推出以下库入门教程：
+ pygame(小游戏制作)
+ opencv-python(计算机视觉)
+ requests(网络爬虫)
+ re(正则表达式)
## 一、什么是Python
### 1.1 python介绍
> Python由荷兰数学和计算机科学研究学会的Guido van Rossum 于1990 年代初设计，作为一门叫做ABC语言的替代品。Python提供了高效的高级数据结构，还能简单有效地面向对象编程。Python语法和动态类型，以及解释型语言的本质，使它成为很多平台上写脚本和快速开发应用的编程语言， 随着版本的不断更新和语言新功能的添加，逐渐被用于独立的、大型项目的开发。 
  Python解释器易于扩展，可以使用C或C++（或者其他可以通过C调用的语言）扩展新的功能和数据类型。Python 也可用于可定制化软件中的扩展程序语言。Python丰富的标准库，提供了适用于各个主要系统平台的源码或机器码。
>> 优点：
>> + 简单、易学、易读、易维护
>> + 用途广泛
>> + 库丰富、代码规范([PEP 8规范](https://www.python.org/dev/peps/pep-0008/))
>> + 高层语言、可移植性强、解释性、可扩展性
>> + 面向对象
>
>> 缺点：
>> + 语法独特，给初学者带来疑惑
>> + 运行速度慢
>> + GIL锁限制线程并行开发
>> + 源代码加密困难
### 1.2 python语法
python为解释性语言，一行一句，书写时无需添加封号( ; )  
```python
# 例1.1
print("hello world!")
```
## 二、Python的变量、类型及运算
### 2.1 变量的定义
python使用非常粗犷的变量定义形式，与c/c++、Java等需要声明变量类型不同，python只需要给出变量值即可
```java
// 例2.1: Java
class JavaTest {
    public static void main(String[] args){
        int str = "hello world";
        System.out.println(str);
    }
}
```
```python
# 例2.2: python
str_ = "hello world"
print(str_)
```
### 2.2 变量的类型
python共有5种变量类型：
+ Number 数字
  + int
  + ~~long~~(python3.x后移除)
  + float
  + complex
+ String 字符串
+ List 列表
+ Tuple 元组
+ Dictionary 字典
+ 特殊：Bool 布尔类型

|类型|实例|
|---|---|
|int|10|
|~~long~~|51924361L|
|float|3.8|
|complex|1-2j|
|string|"hello"|
|list|[1, 2, 3]|
|tuple|(1, 2, 3)|
|dictionary|{"value": 1}|
|bool|True/False|
### 2.3 运算符
#### 2.3.1 算数运算符
|运算符|描述|
|---|---|
|+|加法|
|-|减法|
|*|乘法|
|/|除法，结果为浮点数|
|//|除法，并向下取整|
|%|取模，返回余数|
|**|幂运算|
```python
# 例2.3
a = 45 % 2
# a = 1
b = 5 / 2
# b = 2.5
c = 5 // 2
# c = 2
```
#### 2.3.2 比较运算符
比较运算符返回bool类型

|运算符|描述|
|---|---|
|==|等于|
|!=|不等于|
|\>|大于|
|<|小于|
|\>=|大于等于|
|<=|小于等于|
```python
# 例2.4
print(2 == 3)
# False
print(5 >= 3)
# True
```
#### 2.3.3 赋值运算符
|运算符|描述|
|---|---|
|=|将右边的结果赋值给左边的变量|
|+=|a+=b -- a=a+b|
|-=|a-=b -- a=a-b|
|*=|a*=b -- a=a*b|
|/=|a/=b -- a=a/b|
|//=|a//=b -- a=a//b|
|%=|a%=b -- a=a%b|
|**=|a**=b -- a=a**b|
```python
# 例2.5
a = 1
b = 2
a+=b
# a = 3
```
#### 2.3.4 逻辑运算符
|运算符|描述|
|---|---|
|and|布尔“与”运算符，返回两个变量“与”运算的结果|
|or|布尔“或”运算符，返回两个变量“或”运算的结果|
|not|布尔“非”运算符，返回对变量“非”运算的结果|
```python
# 例2.6
a = True
b = False
print(a and b)
# False
print(not(a and b))
# True
```
#### 2.3.5 位运算符
|运算符|描述|
|---|---|
|&|按位“与”运算符|
|&#124;|按位“或”运算符|
|^|按位“异或”运算符|
|~|按位“取反”运算符|
|<<|“左移动”运算符|
|\>>|“右移动”运算符|
#### 2.3.6 成员运算符
|运算符|描述|
|---|---|
|in|当在指定的序列中找到值时返回True,否则返回False|
|not in|当在指定的序列中没有找到值时返回True,否则返回False|
```python
# 例2.7
a = [1, 2, 4, 6]
print(3 in a)
# False
print(5 not in a)
# True
```
**常用场景：**
```python
# 例2.8
a = [1, 2, 4, 6]
for i in a:
    print(i)
```
#### 2.3.7 身份运算符
|运算符|描述|
|---|---|
|is|当在指定的序列中找到值时返回True,否则返回False|
|is not|当在指定的序列中没有找到值时返回True,否则返回False|
```python
# 例2.9
print(1 is 2)
# False
```
**常用场景：**
```python
# 例2.10
a = True
if a is True:
    pass
```
#### 2.3.8 运算符优先级（略）
熟能生巧，实在不行全用括号括起来
### 2.4 字符串
#### 2.4.1 字符串访问
python索引：

|从前向后|0|1|2|3|4|5|
|---|---|---|---|---|---|---|
|字符串：|a|b|c|d|e|f|
|从后向前|-6|-5|-4|-3|-2|-1|
```python
# 例2.11
# 访问：
text = "abcdef"
print(text[1])
# 结果：b
# 截取：
print(text[1:3])
# 结果：bc
```
#### 2.4.2 字符串拼接
使用`+`拼接字符串
```python
# 例2.12
example = "hello"
print(example + " world")
# hello world
```
#### 2.4.3 字符串运算
|运算符|描述|
|---|---|
|+|字符串拼接|
|*|重复输出字符串|
|[]|字符串索引|
|[:]|字符串切割|
|in/not in|成员运算符|
|r/R|原始字符串|
|%|格式化输出|
#### 2.4.4 常用内置函数
|函数名|描述|
|---|---|
|string.decode()|解码|
|string.encode()|编码|
|string.find()|字符串搜索|
|string.index()|字符串搜索|
|string.format()|格式化|
|string.lower()|转小写|
|string.upper()|转大写|
|string.replace()|替代|
|string.strip()|去除前后空格|
|string.zfill()|填充|
### 2.5 列表
#### 2.5.1 列表访问、拼接、运算
大约与字符串一致
#### 2.5.2 常用内置函数
|函数名|描述|
|---|---|
|list.append()|末尾添加|
|list.count()|统计个数|
|list.index()|列表搜索|
|list.insert()|插入|
|list.pop()|移除|
|list.remove()|删除第一个匹配值|
|list.reverse()|反向排列|
|list.sort()|排序|
```python
# 例2.13
a = ["hello", "world"]
a.append("!")
# a = ["hello", "world", "!"]
a.append(1)
# a = ["hello", "world", "!", 1]
a.append("1")
# a = ["hello", "world", "!", 1, "1"]
```
### 2.6 元组
#### 2.6.1 元组的特殊性质
+ 不可修改
+ 无符号的对象，以逗号隔开，默认为元组
```python
# 例2.14
a = 1, 2
b = (1, 2)
print(a is b)
# True
```
#### 2.6.2 元组的访问、拼接、运算
大约与列表一致
### 2.7 字典
#### 2.7.1 字典定义
`d = {key1 : value1, key2 : value2 , ······}`
#### 2.7.2 字典值访问
通过键进行索引：
`d['key1']` `d['key2']`
#### 2.7.3 字典修改
值的修改：`d['key1'] = value3`
键值对的添加：`d['key4'] = value4`
#### 2.7.4 字典删除
使用`del()`函数
```python
# 例2.15
dict_ = {'Name': 'Zara', 'Age': 7, 'Class': 'First'}
del dict_['Name']    # 删除键是'Name'的条目
# dict_.clear()      # 清空字典所有条目
# del dict_          # 删除字典
print("dict_['Age']: ", dict_['Age'])
print("dict_['School']: ", dict_['School'])
```
#### 2.7.5 字典特性
+ 字典值可以没有限制地取任何python对象，既可以是标准的对象，也可以是用户定义的，但键不行
+ 不允许同一个键出现两次。创建时如果同一个键被赋值两次，后一个值会被记住
+ 键必须不可变，所以可以用数字，字符串或元组充当，所以用列表就不行
## 三、标识符及关键字
python一些具有特殊功能的标识符，即所谓的关键字，是python已经使用过的，所以不允许开发者自己定义和关键字相同的名字的标识符

|and|as|assert|
|---|---|---|
|break|class|continue|
|def|del|elif|
|else|except|exec|
|finally|for|from|
|global|if|in|
|import|is|lambda|
|not|or|pass|
|print|raise|return|
|try|while|with|
|yield|没了|真没了|
## 四、Python输入输出
### 4.1 输入
使用`input()`函数
```python
```
### 4.2 输出
#### 4.2.1 普通输出
使用`print()`
#### 4.2.2 格式化输出
|符号|描述|
|---|---|
|%c|格式化字符及其ASCII码|
|%s|格式化字符串|
|%d|格式化整数|
|%u|格式化无符号整型|
|%o|格式化无符号八进制数|
|%x|格式化无符号十六进制数|
|%X|格式化无符号十六进制数（大写）|
|%f|格式化浮点数字|
|%e|用科学计数法格式化浮点数|
```python
# 例4.1
print("My name is %s and weight is %d kg!" % ('Zara', 21))
# My name is Zara and weight is 21 kg!
```
## 五、条件语句和循环语句
### 5.1 if
结构：if 条件:
```python
# 例5.1
a = 2
if a == 1:  
    pass
elif a is not True:
    pass
else:
    pass
```
### 5.2 while
结构：while 条件:
```python
# 例5.2
count = 0
while count < 9:
   print('The count is:', count)
   count = count + 1
else:
    print("no!")
print("Good bye!")
```
无限循环：
```python
while True:
    print("Yes!")
```
### 5.3 for
结构：for i in sequence:
```python
# 例5.3
for num in range(10, 20):  # 迭代 10 到 20 之间的数字
   for i in range(2, num): # 根据因子迭代
      if num%i == 0:      # 确定第一个因子
         j=num/i          # 计算第二个因子
         print('%d 等于 %d * %d' % (num, i, j))
         break            # 跳出当前循环
   else:                  # 循环的 else 部分
      print(num, '是一个质数')
```
### 5.4 break、continue和pass
#### 5.4.1 break：
> python break语句，就像在C语言中，打破了最小封闭for或while循环。  
  break语句用来终止循环语句，即循环条件没有False条件或者序列还没被完全递归完，也会停止执行循环语句。  
  break语句用在while和for循环中。  
  如果您使用嵌套循环，break语句将停止执行最深层的循环，并开始执行下一行代码。

#### 5.4.2 continue:
> python continue 语句跳出本次循环，而break跳出整个循环。  
  continue 语句用来告诉Python跳过当前循环的剩余语句，然后继续进行下一轮循环。  
  continue语句用在while和for循环中。

#### 5.4.3 pass:
> python pass 是空语句，是为了保持程序结构的完整性。  
  pass 不做任何事情，一般用做占位语句。
## 六、函数
### 6.1 函数定义
格式：`def 函数名(参数1, 参数2, ······):`  
使用：`return`返回想要的参数
```python
# 例6.1
def printf(num):
    print(num)
```
### 6.2 函数调用
格式：`函数名(参数1, 参数2, ······)`
```python
# 例6.2
def printf(num):
    print(num)
printf(1)
# 1
```
### 6.3 参数传递
参数有两种：
+ 不可更改参数
+ 可更改参数
> 对于不可更改参数，传值时新建了一个对象，并将值赋给了新对象，原参数值没有发生变化。  
> 对于可更改参数，传值时则是全部传过去，修改时直接修改原数据。

```python
# 例6.3：不可更改
def change_int(a):
    a = 10
b = 2
change_int(b)
print(b)
# 结果是 2
```
```python
# 例6.4：可更改
def changeme(my_list):
   my_list.append([1,2,3,4])
   print("函数内取值: ", mylist)
   return
mylist = [10,20,30]
changeme(mylist)
print("函数外取值: ", mylist)
# 函数内取值:  [10, 20, 30, [1, 2, 3, 4]]
# 函数外取值:  [10, 20, 30, [1, 2, 3, 4]]
```
### 6.4 参数类型（略）
共有4种参数：
+ 必备参数
+ 关键字参数
+ 默认参数
+ 不定长参数
### 6.5 作用域
+ 全局变量
+ 局部变量
```python
# 例6.5
total = 0 # 这是一个全局变量
# 可写函数说明
def sum_(arg1, arg2):
   total = arg1 + arg2 # total在这里是局部变量.
   print("函数内是局部变量 : ", total)
   return total
 
#调用sum函数
sum_(10, 20)
print("函数外是全局变量 : ", total)
# 函数内是局部变量 :  30
# 函数内是全局变量 :  0
```
## 七、模块导入
第一种是直接import，导入整个模块  
第二种是仅导入某个函数或变量  
如下面的代码片段：
```python
import requests
from bs4 import BeautifulSoup
```
## 八、文件I/O
### 8.1 `open()`方法
`file object = open(file_name [, access_mode][, buffering])`

其中：
+ file_name为文件名
+ access_mode为打开文件的模式
### 8.2 文件操作模式
|符号|模式描述|
|---|---|
|t|文本模式|
|x|写模式，若存在文件则报错|
|b|二进制模式|
|r|只读模式|
|rb|二进制只读模式，指针位于开头|
|r+|用于读写，指针位于开头|
|rb+|二进制读写模式，指针位于开头|
|w|写入模式，覆盖原有内容，能新建文件|
|wb|二进制写入，覆盖，能新建|
|w+|读写模式，覆盖，能新建文件|
|wb+|二进制读写，覆盖，能新建|
|a|追加模式，能新建|
|ab|二进制追加，能新建|
|a+|读写追加，能新建|
|ab+|二进制读写追加，能新建|
### 8.3 使用方法
在文件操作过程中，涉及到`open() close()`等IO操作，为了防止新手出现操作失误，python提供了便捷的方法
```python
# 例8.1
with open("test.txt", "a+") as f:
    f.write("hello world")
# 单独使用open函数对文件进行操作时，还需要close函数关闭IO接口  
# 但是使用with open时，会自动进行close操作，无需再次close
```
## 九、异常抛出
### 9.1 结构
```python
try:  # 尝试运行语句
    pass
except (IndexError, ValueError):  # 捕获该异常，分析后继续运行
    pass
else:  # 没有异常的话，运行语句（可选）
    pass
```
### 9.2 常见异常
|KeyboardInterrupt|Exception|AttributeError|
|---|---|---|
|EOFError|IOError|ImportError|
|IndexError|NameError|SyntaxError|
|IndentationError|TabError|ValueError|
|UnicodeError|OSError|StandardError|
## 十、Python基础挑战题！
定义一系列函数，使得调用函数时，可以在根目录下生成一个"triangle.txt"文件，并在txt文件中画出杨辉三角，要求杨辉三角显示行数在函数的参数中。
> 例：行数为4，输出：  
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1  
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1&nbsp;&nbsp;&nbsp;&nbsp;1  
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1&nbsp;&nbsp;&nbsp;&nbsp;2&nbsp;&nbsp;&nbsp;&nbsp;1  
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1&nbsp;&nbsp;&nbsp;&nbsp;3&nbsp;&nbsp;&nbsp;&nbsp;3&nbsp;&nbsp;&nbsp;&nbsp;1  
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;······
## 十一、学习网站
+ [菜鸟](https://www.runoob.com/python/python-tutorial.html) 
## 十二、总结
+ 认真看完这份教程，并跟随例题训练，举一反三尝试，那么恭喜你，成功入门并初步掌握了python这门奇妙的语言！
+ 其实这份教程不完全是基础用法的讲解，还有很多如字符串操作、内置函数等，都是需要不断实践、记住的，因此教程中仅仅列举或提及。  
+ 最后，祝各位同学学习顺利！（本教程搭配模块专精教程更佳哦～）
