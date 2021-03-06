> 刘春明 [博客](http://blog.csdn.net/liuchunming033)

## 认识Python
Python 是一门面向对象、解释型编程语言，在近10年的TIOBE排行榜上一直处于上升趋势。
Python语言免费、开源、跨平台、易学、易懂、易维护、强大，以优雅著称。
具有应用广泛场景，可以应用到web开发、自动化测试、运维、数据分析、科学计算、人工智能，只有你想不到，没有python做不到。
### Python语言特点
1.解释型脚本语言
2.面向对象的语言
3.动态语言，变量本身的数据类型是不固定的，可以给变量赋予任何类型的数据。
4.不用考虑内存问题
5.默认编码是UTF-8编码

### 下载和安装
在操作系统的终端命令行上，输入python并按回车键，如果能够进入到python交互式开发环境，则表示python已经在该电脑上安装了。
如果电脑上没有安装python，则可以手动安装。
#### Windows下安装
安装方法如下，
安装完成后，设置环境变量
#### Mac下安装
Mac操作系统自带python，不过版本python2.7，如果你需要其他版本的python，则需要手动安装。安装方法如下
#### Linux下安装
Linux操作系统中也自带python，版本也是python2，如果你需要其他版本的python，则需要手动安装。安装方法如下

### 运行Python程序
#### 交互式执行
执行Python程序有两种方式，一种是在python的交互式环境中，例如，输入
```
print('Hello world!')
```
按回车键就会执行上面的python程序。
#### 脚本形式执行
另外一种，也是最常用的方式是通过脚本方式执行python。
将print('Hello world!')写入hello.py，在命令行下执行python hello.py。
更通用的方式是在脚本文件的首行加上python解释器的路径，一种是通过env命令去查找Python解释器：
```
#!/usr/bin/env python
```
另外一种是通过直接指定Python解释器的路径
```
#!/usr/local/bin/python
```
之后将脚本文件的属性改成具有可执行权限，
```
chmod 755 *.py
```
接下来就可以直接执行python脚本了，方法是在命令行输入脚本名并且按回车。
```
*.py
```

### 基本语法
#### 缩进
python使用缩进来区分代码块，缩进的空白数量是可变的，但必须统一，通常使用四个空格作为一级缩进
#### 跨行与并行
可以使用斜杠（ \）将一行的语句分为多行显示，多行语句合并成一行时，不同于局要用分号;隔开
#### 注释
python中单行注释采用 # 开头，多行注释使用三个单引号(''')或三个双引号(""")。
#### 变量和赋值
变量由字母、数字和下划线构成标识符，不能以数字开头，大小写敏感。
python有很多内置的标识符，自定义的变量一定要避免与这些内置的标识符重名。
以双下划线开头和结尾的 __foo__ 代表 Python 里特殊方法专用的标识，尽量避免命名类似的变量。
Python 是动态类型语言， 也就是说不需要预先声明变量的类型。 变量赋值通过等号来执行。
允许同时为多个变量赋值，多个变量赋相同值，
```
a = b = c = 1
```
多个对象指定多个变量
```
a, b, c = 1, 2, "john"
```
### 运算符
#### 算术运算符
假设变量a为10，变量b为21
```
a + b # 输出结果 31
a - b # 输出结果 -11
a * b # 输出结果 210
b / a # 输出结果 2.1
b % a # 输出结果 1
a**b # 为10的21次方
9//2 # 输出结果 4 , 9.0//2.0 输出结果 4.0
```
#### 比较运算符
假设变量a为10，变量b为20
```
(a == b) # 返回 False
(a != b) # 返回 True
(a > b) # 返回 False
(a < b) # 返回 True
(a >= b) # 返回 False
(a <= b) # 返回 True
```
#### 赋值运算符
假设变量a为10，变量b为20
```
c = a + b # 将 a + b 的运算结果赋值为 c
c += a # 等效于 c = c + a
c -= a # 等效于 c = c - a
c *= a # 等效于 c = c * a
c /= a # 等效于 c = c / a
c %= a # 等效于 c = c % a
c **= a # 等效于 c = c ** a
c //= a # 等效于 c = c // a
```
#### 位运算符
位运算符，是把数字看作二进制来进行计算的，假设变量 a 为 60，b 为 13
```
(a & b) # 输出结果 12 ，二进制解释： 0000 1100
(a | b) # 输出结果 61 ，二进制解释： 0011 1101
(a ^ b) # 输出结果 49 ，二进制解释： 0011 0001
(~a ) # 输出结果 -61 ，二进制解释： 1100 0011， 在一个有符号二进制数的补码形式。
a << 2 # 输出结果 240 ，二进制解释： 1111 0000
a >> 2 # 输出结果 15 ，二进制解释： 0000 1111
```
#### 逻辑运算符
假设变量 a 为 10，b为 20
```
x and y #  如果 x 为 False，x and y 返回 False，否则它返回 y 的计算值。(a and b) 返回 20
x or y #  如果 x 是 True，它返回 x 的值，否则它返回 y 的计算值。(a or b) 返回 10
not x #  如果 x 为 True，返回 False 。如果 x 为 False，它返回 True。not a 返回 False
```
#### 成员运算符
成员运算符，假设a为1，b为[1,2,3]
```
a in b # 返回True
a not in b # 返回False
```
#### 身份运算符
身份运算符，用于比较两个对象的存储单元
```
x is y # 类似 id(x) == id(y) , 如果引用的是同一个对象则返回 True，否则返回 False
x is not y # 类似 id(a) != id(b)。如果引用的不是同一个对象则返回结果 True，否则返回 False。
```
以上运算符的优先级不同，为了方便控制，建议使用小括号()更改优先级顺序。比如

### 开发环境
文本编辑器Atom、IDE推荐Pycharm