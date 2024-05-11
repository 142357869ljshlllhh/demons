---
title: python学习
date: 2024-01-20 23:06:05
tags:
---

# 前言

python在高中时学习过一些入门知识，也是下面的大部分知识，很久没有接触，大多都忘记了，虽然我的专业是计算机科学与技术，但Python的学习还不知要到什么时候，还好上学期已经学习了c语言的一些基础知识，再加上高中有所基础，所以自学python的基础知识对我来说并不困难，这篇blog记录我的学习过程。

# 一、数据

## 1.数值

1. 整数类型：int

常见运算+、-、*

- 整除：//

- 除：/

- 取余：%

- divmod(m,n)   得到两个整数，一个是m//n,一个是m%n

- m**n   m的n次方

- abs(m)     求绝对值

比较：== ; > ; >= ; < ; <= ;

2. 浮点型：float

3. 复数类型:     (1+3j)*(2+3j)=(-4+7j)

复数之间只能比较是否相等

4. 字符串类型：str   用双引号或者单引号成对都可以表示字符串；多行字符串用三个连续单引号表示，如'''abc
   
   def‘’‘
   
   第一个字符编号为0
   
   - 获取字符串长度：len函数
   
   - 切片操作：s[start：end：step]  start、end、step：三个数
   
   - +：两个字符串连接
   
   - *：将字符串重复若干次  如： "abc"*2="abcabc"
   
   - == 判断是否相同
   
   - in：判断字符串中是否包含某个字符串 如："h" in a
     
     常见字符串操作
     
     1. chr() : 输入ASCII值得到字符
     
     2. ord() : 输出字符的ASCII值
     
     3. str.strip：去掉字符串前后空格，内部空格不受影响
     
     4. str.lstrip：去除字符串前部的所有空格
     
     5. str.rstrip：去掉字符串后部的所有空格
     
     6. str.isalpha：判断字符串是否全部由字母组成
     
     7. str.isdight：判断字符串是否全部由数字构成
     
     8. str.isalnum：判断字符串是否仅由字母和数字组成
        
        字符串高级操作
        
        1. replace：替换子串
           
           - "Tom smiled,Tom,cried".replace('Tom','Jane')  :  'Jane smiled,Jane cried'
        
        2. upper/center/swapcase：大小写相关
           
           - 'abc'.upper()  :  'ABC'
           
           - 'aBC'.lower()  :  'abc'
           
           - 'Abc'.swapcase()  :  'aBC'
        
        3. join：合并
           
           '-'.join(["One","for","Two"])  :  'One-for-Two'
        
        4. split：分割
           
           'You are my sushine.'.split(' ')   :    ['You','are','my','sunshine.']

5. 转义符号：\  
   
   - 如换行：\n
   
   - 两个\\\表示\本身

6. 数学函数：math模块：import math（处理整型和浮点型）
- 数学常数：圆周率，自然对数的底数

- 三角函数、对数、最大公约数、最小公倍数等

## 2.逻辑值（bool）

1. 逻辑值只包括真和假两个值
   
   - 整数、浮点数和复数：0为false，所有非0值都为true
   
   - 字符串类型：空串（”“）为false，所有非空串都是true
   
   - 所有序列类型：空序列为false，所有非空序列都是true
   
   - 空值None 表示无意义或不知道，也是false

2. 逻辑运算
- ”与“ : and （and连接的两个真值同时为真，计算结果才为真）

- "或"：or  （or连接的两个真值只要有一个为真，计算结果就为真）

- ”非“： not （not 连接的一个真值，非真为假，非假为真）

- 优先级：not 最高，and次之，or最低

## 3.变量

1. 命名规则
   
   - 字母和数字组合，”_"算字母，字母区分大小写，不带特殊符号（空格、标点、运算符等）
   
   - 名字第一个字符必须是字母（python中汉字算字母）

2. 赋值
   
   - 最基本赋值语句
   
   - 合并赋值： a=b=c=1
   
   - 按顺序依次赋值： a,b,c=7,8,9
   
   - 简写赋值语句： a+=1 ; a*=1.5 ; a/= 3

3. 进制
   
   - hex()十六进制
   
   - cot()八进制
   
   - bin()二进制

# 二、容器

## 1.列表和元组

- 列表可变可更新，元组是不可变序列（去掉灵活性换取性能）

- 元素类型没有限制
1. 创建列表：[] 、 list()

       创建元组:   () 、 tuple()

2. 增长列表：
   
   - append：列表末尾加上一个：alist.append(item)
   
   - insert： 列表中间任意一个地方添加: alist.insert(i,item)
   
   - extend：将两个列表连接

3. 缩减列表：
   
   - pop：指定去除一个元素并返回其值: alist.pop(i)  不指定则去除列表最后一个，并返回其值：alist.pop()
   
   - remove：指定一个数据值（删除首次出现的那个）：alist.remove("item")
   
   - clear：变成空列表

4. - reverse：把列表头尾重新反转排列:  alist.reverse()
   
   - sort：把列表的数据元素按照大小顺序重新排列（从小到大）：alist.sort()
   
   - reversed/sorted：得到重新排列的列表，而不影响原来的列表
   
   - count：返回item在列表中出现的次数： alist.count(item)
   
   - del：删除第i个元素：del alist[i]
   
   - index：找到item在列表中首次出现位置：alist.index(item)
   
   - len(alist)

5. 合并：
   
   - 加法运算+：连接两个列表/元组（生成新的列表，不影响原来两个列表/元组）
   
   - 乘法运算*：复制n次，生成新列表/元组

6. 列表切片：alist[ start : end : step] 或 atuple[start : end : step]

7. 计算：
   
   - sum函数：列表所有数据元素累加
   
   - min/max函数：返回列表中最小/最大的数据元素

## 2.集合

1. 创建集合：{}或者set()     
   
   - 集合会自动忽略重复的数据
   
   - 集合不能加入可变类型数据

2. 增长集合：
   
   - add：添加一个数据：  aset,add(item)
   
   - update：批量添加数据： aset.upset

3. 缩减集合
   
   - clear： 清空集合： aset.clear（）
   
   - pop：删除任意一个数据并提供其值作为返回值输出：aset,pop()
   
   - remove/discard：删除指定数据： aset.remove(item)
     
     remove一个不存在的元素时会报错，discard一个不存在的元素时不会报错

4. 集合大小：len函数

5. in：判断元素是否属于集合

6. 运算：
   
   - 并：a|b
   
   - 交：a&b
   
   - 差：a-b
   
   - 对称差：a^b： a-b|b-a

7. 关系判定：<= , < ,= , >= , >:子集/真子集/相等/超集/真超集

       isdisjoint()：判断两交集是否为空：a.isdisjoint(b)

## 3.数据类型

### 1.灵活性强会花费一些计算或者存储的代价去维持这些强大的功能

1. 不可变类型（一旦创建就无法修改数据值的数据类型）：整数、浮点数、复数、字符串、逻辑值、元组

2. 可变类型（可以随时改变的数据类型）：列表、字典、集合

### 2. 字典的类型可以是任意不可变类型

- 用元组作为坐标，索引元素：poi={(100,100):'bus stop'}     
  
  索引：poi[(100.100)]

# 二.输入和输出

## 1.input函数

- input(prompt[^1])         1.提示信息
  
  例：x= input('x:')

**input()返回值是字符串**，可通过int()函数将字符串类型强制转换为整数类型

## 2.print函数

- print([object,...][,sep[^1]=''][,end[^2]='\n'][,file[^3]=sys.stdout])
1. 表示变量之间用什么字符串隔开，缺省是空格

2. 表示以这个字符串结尾，缺省为换行

3. file：指定了文本将要发送到的文件、标准流或其他类似文件的对象；默认是sys.stdout

### 3.格式化字符串

- %d：整数    %s：字符串    %f：浮点数
  
  - '%d %s'%(23,'hello')     '23 hello'
  
  - '%d'%(23,[^1])             '23'      1.单个字符需要在最后加逗号
  
  - '(%4d):K:%s'%(12,'Hello')           '(  12):K:Hello'
  
  - '(%04d):K:%s'%(12,'Hello')              '(0012):K:Hello'

%前面加-则为左对齐

# 三、计算和控制流

## 1.条件分支语句（if）

- if <逻辑表达式>:
  
      <语句块1>
  
      ......
  
  else:
  
      <语句块2>
1. 冒号表示语句层次

2. 语句块必须缩进
- 多种情况的条件语句：elif语句
  
  if <逻辑表达式1>:
  
      <语句块1>
  
  elif <逻辑表达式2>:
  
      <语句块2>
  
  else:
  
      <语句块3>

## 2.条件循环语句（while）

- while<逻辑表达式[^值为true则循环]>:
  
      <语句块>

            break[^1]         1.跳出循环

            continue[^2]    2.略过余下循环语句

            <语句块>

        else[^3]：             3.条件不满足退出循环，则执行

             <语句块>

中断程序循环：CTRL+C

## 3.迭代循环（for）

- for <循环变量[^普通变量]> in <可迭代对象[^1]>:
  
      <语句块1>
  
      break                跳出循环
  
      continue          略过余下循环语句

            <语句块2>

        else:                     迭代完毕，则执行

            <语句块3>

1.可为列表、字典、元组

## range函数

- range(<终点>)             返回一个从零到终点的数列（**不包含终点**）

- range(<起点>,<终点>)            从0以外的任何整数开始构建数列（**包含起点不包含终点**）

- range(<起点>,<终点>,<步长>)       修改数列的步长，通过将步长设置为复数能够实现反向数列

range类型的对象：可直接当作序列或转换成list或tuple等容器类型

## 4.代码组织：函数（def）

1. 定义函数：
   
   - 用def语句创建一个函数
     
     - 用return关键字指定函数返回值
       
       def <函数名> (<参数表>):
       
            <缩进的代码段>
       
           return <函数返回值>
     
     - 调用函数:
       
       <函数名>(<参数>)
       
       - 无返回值： <函数名>(<参数表>)
       
       - 返回值赋值：v = <函数名>(<参数表>)

2. - 局部变量：在函数内部定义的参数和变量：只在该函数定义范围内有效
   
   - 全局变量：在函数外部定义的，作用域是整个代码段
     
     在函数内部使用与全局变量同名的变量时，若未在函数内进行定义，则使用全局变量的值，局部变量的值不会影响全局变量的值

## 5.map函数（对列表中每一个元素做一个相同的处理，得到新处理）

- map(fuc,list1,list2)
  
  - 例如列表每个值都乘以3：
    
    num  = [10,20,40,80,160]
    
    def mul3(a):
    
        return a*3
    
    print (list(map(mul3,num)))

## 6.匿名函数(lambada)

- 有时函数只用一次，其名称也不重要，可以无需费神去def一个

- 表达式
  
  - lambda <参数表>：<表达式>

## 7.函数的参数

- 参数：传入到函数的值
  
  - 形式参数：函数创建和定义过程中，函数名后面括号里的参数
    
    只是代表一个位置、一个变量名
    
    1. 可变参数
       
       - def func(*args)：#不带key的多个参数（未知，多少都可以）（元组列表等）
       
       - def func(**kwargs)：#key=val形式的多个参数（字典等）
    
    2. 固定参数
       
       - def func(key1,key2,key3...)
         
         - 位置参数：按照前后顺序对应到函数参数传入
           
           func（arg1.arg2...)
         
         - 关键字参数：由于指定了key，可以不按照顺序对应
           
           func(key1=arg1,key2=arg2...)
         
         - 混用：所有位置参数必须在前，关键字参数必须在后
  
  - 实际参数：函数在调用时传入的参数
    
    一个具体内容，赋值到变量的值

# 四、引用拓展模块

1. 模块引用方式
   
   1. import <模块> [as<别名>]      使用时要加上命名空间
   
   2. from <模块> import <函数>     引用模块中的某个函数，调用时不需要再加上命名空间

2. 标准库：
   
   1. 加密服务
      
      - hashilib：安全哈希和消息摘要算法接口
      
      - hamc：用于消息身份验证的密钥哈希算法
      
      - secrets：生成用于管理机密的安全随机数
   
   2. 并发执行
      
      - threading：基于线程的并发性
      
      - multiprocessing：基于进程的并发性
      
      - concurrent.futures：启动并行任务
      
      - subprovess：子流程管理
      
      - sched：事件的调度程序
      
      - queue：同步的队列类
      
      - _thread：低级线程ApI
   
   3. 通用系统服务
      
      - os：其他操作系统接口
      
      - io：用于处理流的核心工具
      
      - time：时间访问和转换
      
      - argparse：用于命令行选项，参数和子命令的解析器
      
      - getopt：用于命令行选项的c风格解析器
      
      - logging：Python的日志记录工具
      
      - getpass：便携式密码输入
      
      - cuises：字符单元格显示的终端处理
      
      - platform：访问底层平台的标识数据
      
      - errno：标准errno系统符号
      
      - ctypes：Python的外部函数库
   
   4. 文件和目录访问
      
      - pathlib：面向对象的文件系统路径
      
      - os.path：常见的路径名操作
      
      - fileinput：迭代多个输入流中的行
      
      - stat：解释stat（）结果
      
      - filecmp：文件和目录比较
      
      - tempfile：生成临时文件和目录
      
      - glob：Unix样式路径名模式拓展
      
      - fnmatch：Unix文件名模式匹配
      
      - linecache：随机访问文本行
      
      - shutil：高级文件操作
      
      - macpath：Mac OS 9路径操作函数
   
   5. 文件格式
      
      - csv：CSV文件读写
      
      - configparser：配置文件解析器
      
      - netrc：netrc文件处理
      
      - xdrlib：对XDR数据进行编码和解码
      
      - plistlib：生成并解析MAC OS X.plist文件
   
   6. 数据压缩和存档
      
      - zlib：与gzip兼容的压缩
      
      - gzip/bz2：支持gazip/bzilp2文件
      
      - lzma：使用LZMA算法进行压缩
      
      - zipfile：使用在ZIP存档
      
      - tarfile：读取和写入tar归档文件
   
   7. 数据持久化：
      
      - pickle：python对象序列化
      
      - copyreg：注册pickle支持功能
      
      - shelve：python对象持久化
      
      - marshal：内部python对象序列化
      
      - dbm：与unix”数据库“的接口
      
      - sqlite3：sqlite数据库的DB-API 2.0接口
   
   8. 功能编程模块：
      
      - itertools：为搞笑i循环创建迭代器的函数
      
      - functools：可调用对象的高阶函数和操作
      
      - opertor：标准运算符作为函数
   
   9. 数据类型：
      
      - datetime：基本日期和时间类型
        
        ### 1.时间
        
        1. datetime.date()：处理日期（年月日）
           
           - 修改日期格式：strftime
             
             例如：datetime.date.today().strftime('%Y-%m-%d %H:%M:%S')
             
             输出为'2024-01-27 00:00:00'
             
             - 修改为国际标准格式：datetime.datetime.now().isoformat()
           
           - 获取今天的日期：
             
             datetime.date.today()
             
             datetiem.datetime.now()
        
        2. datetime.time()：处理时间（时分秒、毫秒）
        
        3. datetime.datetime()：处理日期+时间
        
        4. datetime.timedelta()：处理时段（时间间隔）
        
        ### 2.时间戳
        
        指格林威治时间1970年1月1日00时00分00秒其至现在的总秒数
        
        1. 将时间戳转换成日期：
           
           datetime.date.fromtimestamp()
        
        2. 将日期转换为时间戳：
           
           timetuple函数
           
           返回秒数来表示时间的浮点数：time.mktime函数
        
        ### 3.时间上的加减法
        
        1. timedelta()：表示两个时间点的间隔
           
           例如：
           
           today = datetime.datetime.now()
           
           yesterday = today - datetime.tiemdelta(days=1)
           
           hours = today - datetime,timedelta(hours=1)
      
      - calendar：与日历相关的一般功能
        
        1. calendar.calendar(年)
           
           calendar.month(年，月)
           
           calendar.prmonth(年，月)=print(calendar.month(年，月))
           
           calendar.prcal(年)= print(calendar.calendar(年))
        
        2. 将日历列表化:calendar,monthcalendar()：嵌套列表，最里层列表有七个元素，代表一周,如果没有本月日期，则为0
        
        3. 判断闰年：calendar.isleap(年)
        
        4. 计算某月共有几天，从周几开始：
           
           例如：calendar.monthrange(2024，2)
           
           输出为(calendar.THURSDAY, 29)
        
        5. 计算
      
      - collections：容器数据类型
      
      - heapq：堆队列算法
      
      - bisect：数组二分算法
      
      - array：高效的数值数组
      
      - weakref：弱引用
      
      - types：动态类型创建和内置类型的名称
      
      - copy：浅层和深层复制操作
      
      - pprint：格式化输出
      
      - reprlib：备用repr（）实现
      
      - enum：支持枚举
   
   10. 数字模块：
       
       - numbers：数字抽象基类
       
       - math：数学函数
       
       - cmath：复数的数学函数
       
       - decimal：十进制定点和浮点算术
       
       - fractions：有理数
       
       - random：生成伪随机数
       
       - statistics：数学统计功能
