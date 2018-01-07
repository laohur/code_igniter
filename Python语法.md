Python语法

1.python的由来

python是Van
Rossum于1989年设计的解释型高级语言，特性是快速实现，直接调用，抽象程度高，效率低。随着计算机趋贱和程序员趋贵，python正由于便利性越来越多地应用在效率要求低的场合中，尤其是原型实现。

2.python开发环境

windows系统，python.org官网中下载最新python，全选安装，打开idle，file-\>new
file。将hello.py的代码逐字敲入编辑器中，执行菜单-\>run
mode.正确的话会输入一个字符串和数字，返回一句话。

3.python程序结构

hello.py 源代码

\# file: D:/code/hello.py

\# author: pythoneer

\# create_time: 2017-12-12

\# \#开头为注释行，注释删除开不影响执行

\# 若有import os，表示引用os.py文件

\# python用四空格缩进和:区分代码块；多数语言用{}及;区分代码块

class Student(): \# classname(parentclass)

def learn(self, name, hour): \# 用def 定义一个函数，class定义一个类

\# print("hour: ") \# 监测name变量，用于调试

\# print(hour) \# 动态语言边解释边执行，不需要提前声明变量

print("%s will learn %d hours everyday!" %(name, hour%13) ) \#
%与数学上的意义不同，程序语言中意义也不同

\# 打印函数参数如上：%s表示此位置将输出一个字符串，%d是整数，传输参数时%前无,
后跟一个元组格式参数

return 0 \# 函数结束

name = input("my name is :") \#变量名称可以包含字母、_、数字，数字不可用于开头。

hour = int(input("lucky number :"))

learner = Student() \# 实例化类Student()，注意有()

learner.learn(name, hour) \# 执行函数

3. python数据类型

常见的Python的基本数据类型有integer、float、string，无需提前声明，使用时再赋值也可以。

可以转换int(7.5)返回整数7。

’string’[-1]结果为’g’。”hah %d \\n”双引号中会检查匹配变量，\\n表示换行。

是非类型有两个值True、False,判断其他类型变量只有0才会被自动转化为False，其余一般为True。

常见的复合类型有list、dict(dictionary)、tuple。

list只能序号索引，dict可以任意键索引，tuple一条不变的记录。

定义：

list=[1,2][2,3,6]

tuple=(‘as’,’sd’)

dict={key:value, “id”:’name’}

访问：

list[1][2]

for k,v in dict:

prinf(k)

print(v)

4. 运算符号

variable=3.5表示给变量variable赋值3.5，=表示赋值。var+=3表示var=var+3.

==表示相等。

var++表示var=var+1。‘ha’+’hei’结果为’hahei’

\*表示x，‘a’\*3的效果是‘aaa’。n\*\*m 表示n的m次方

/表示÷。

67%13求67/13的余数。%另一个作用是表示占位类型。

4\<\<1表示4的二进制形式按位左移1位，舍去容器外的高位，新增地位为0，4在这里不会舍弃高位，4左移1位后为8，相当于乘上2.，二进制乘上10
.\>\>1的效果是除以2.

&按位与，\|按位或，\~按位非。

5. 流程控制

If true_expression:

excute statemen1t

elif

statement2

else

statement3

&&
相当于and逻辑运算，\|\|相当于or或运算，！相当于逻辑非。可以直接连用\<=表示小于等于。\<\>和！=都表示不等于。

a == 2? statement1: statement2 若a=2，则执行statement1，否则执行statement2。

for index in range(1,5): 相当于其他语言中的for(int i=1; i\<=5; i++){}.

while 、do while 、loop、switch等与其他语言类似。

while a\<2 \# 符合条件则下一步

a++

if a=1

continue \# 调到while重新开始

if a=0

breakl \# 结束本代码块

switch value:

case 2:

statement1 \# 若value==2，则执行

case 3:

break \# 若value==3，则跳出

default:

statement2 \# value不是case列举值，执行statement2

6. 文件管理

import os \# 引入operating system包以便操作外部文件

line=”I created a file!”

If os.path.exist(“D:/output.txt”) \# 检查文件是否存在

file=open(“D:/output.txt”) \# 新建文件对象file

print(file.read())

else

file=open(“D:/output.txt”,”w”) \#
w表示直接写一个D:/output.txt，如果有旧文件则覆盖。

file.write(line) \# 程序结束时自动释放文件连接

推荐书目：入门《像计算机科学家一样思考python》

练习：《python cookbook》
