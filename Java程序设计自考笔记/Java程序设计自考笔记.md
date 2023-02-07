# Java程序设计自考笔记

## 目录

-   [第一章: java概述](#第一章-java概述)
    -   [Java语言起源](#Java语言起源)

    -   [Java语言的特点](#Java语言的特点)

    -   [Java开发环境的安装及配置](#Java开发环境的安装及配置)

    -   [Java API文档](#Java-API文档)

-   [第二章: 数据和表达式](#第二章-数据和表达式)
    -   [基本语法元素](#基本语法元素)

    -   [基本数据类型](#基本数据类型)

    -   [表达式](#表达式)

-   [第三章: 流程控制语句 ](#第三章-流程控制语句)
    -   [Java程序的结构](#Java程序的结构)

    -   [流程控制](#流程控制)

    -   [简单的输入/输出](#简单的输入输出)

    -   [处理异常](#处理异常)

-   [第四章: 面向对象程序设计](#第四章-面向对象程序设计)
    -   [类和对象](#类和对象)

    -   [包装类](#包装类)

-   [第五章: 数组和字符串](#第五章-数组和字符串)
    -   [数组](#数组)

    -   [字符串](#字符串)

    -   [Vector类](#Vector类)

-   [第六章: 继承和多态](#第六章-继承和多态)
    -   [子类](#子类)

    -   [方法覆盖与多态](#方法覆盖与多态)

    -   [终极类与抽象类](#终极类与抽象类)

    -   [接口](#接口)

-   [第七章: 输入和输出流](#第七章-输入和输出流)
    -   [数据流基本概念](#数据流基本概念)

    -   [基本字节数据流](#基本字节数据流)

-   [第八章: 图形界面设计](#第八章-图形界面设计)
    -   [AWT和Swing](#AWT和Swing)

    -   [容器](#容器)

    -   [标签及按钮](#标签及按钮)

    -   [布局管理器](#布局管理器)

    -   [事件处理](#事件处理)

    -   [绘图基础](#绘图基础)

-   [第九章: Swing组件](#第九章-Swing组件)
    -   [列表(JList): ](#列表JList-)

    -   [文本域(JTextField)](#文本域JTextField)

    -   [文本区(JTextArea)](#文本区JTextArea)

    -   [菜单栏及菜单](#菜单栏及菜单)

    -   [菜单项(JMenuItem)](#菜单项JMenuItem)

    -   [复选菜单项(JCheckBoxMenuItem)](#复选菜单项JCheckBoxMenuItem)

    -   [单选菜单项(JRadioButtonMenuItem)](#单选菜单项JRadioButtonMenuItem)

    -   [对话框(JDialog)](#对话框JDialog)

    -   [标准对话框(JOptionPane)](#标准对话框JOptionPane)

    -   [文件对话框(JFileChooser)](#文件对话框JFileChooser)

-   [第十章: 多线程](#第十章-多线程)
    -   [线程和多线程](#线程和多线程)

    -   [创建线程](#创建线程)

    -   [线程基本控制](#线程基本控制)


## 第一章: java概述

### Java语言起源

-   前身Oak语言1991年, 1995年改为Java
-   美国Sun公司
-   Java语言基本概念
    -   面向对象的程序设计语言
    -   与机器无关的二进制格式的文件
    -   Java虚拟机(JVM): 是一台虚拟机,是通过在实际计算机上仿真模拟各种计算机功能实现的
    -   完整的程序包软件

### Java语言的特点

-   语法简单,功能强大,安全可靠
-   与平台无关
-   编译和解释两种运行方式
    -   即时编译功能( just in time JIT)
    -   Java程序编译成的是虚拟机能够识别的字节码, 它就是虚拟机的机器指令，与平台无关,有统一的格式,不依赖于具体的硬件环境,只运行在JVM上
-   多线程
-   动态执行兼有丰富的API文档及类库

### Java开发环境的安装及配置

-   在配置完JDK(java语言软件开发工具包)环境变量后,输入javac确定是否完成安装
-   IDE(集成开发环境)
-   Java环境基本构件
    -   javac: Java编译器
    -   java: Java解释器
    -   jdb: java调试器
    -   javap: 反编译器
    -   javadoc: 文档生成器

Java程序示例

-   分类: Java应用程序和Java小应用程序
-   Java程序文件(源文件)的扩展名.java, 编译后生成的字节码文件(类文件)的扩展名.class
-   Java执行系统是不能识别源文件，只识别.class文件
-   一个文件中只能有一个公有类,且文件名要与类名要完全一致
-   运行: Java解释器执行类文件 例 java HelloWorldApp

Java中的面向对象技术

-   面向对象分析(Object-Oriented Analysis OOA)、面向对象设计(Object-Oriented Design OOD)、面向对象的程序设计(Object-Oriented Programming OOP)
-   多态性: 在一个类或多个类中,可以让多个方法使用一个名字

### Java API文档

-   java.lang
    -   java.lang.Math
    -   java.lang.String
    -   java.lang.StringBuffer
    -   java.lang.StringBuilder
-   java.awt
    -   java.awt.Window
    -   java.awt.Panel
    -   java.awt.Frame
    -   java.awt.Button
-   java.lang.Math
    -   Math.sin
    -   Math.cos
    -   Math.tan
    -   Math.asin
-   java.lang.String
    -   equals
    -   length
    -   indexOf
    -   lastIndexOf
-   java.util.Random
    -   nextFloat
    -   nextDouble
-   java.awt.Color
    -   getRed
    -   getGreen
    -   getBlue

# 第二章: 数据和表达式

### 基本语法元素

-   空间、注释及语句
    -   换行符和回车符都可以表示一行结束
    -   空白和Tab键都是空白
    -   /\*\* 文档注释 \*/
    -   语句是java程序的最小单位,程序各语句以";"分隔
    -   成对大括号"{"和"}"包含的一系列语句,称为语句块,简称为块
-   未使用预留关键字: cast、const、future、generic、goto、inner、operator、outer、rest、var
-   标识符: 由字母、数字、下划线、或美元符号组成,数字不能作为标识符开头
    -   Java代码使用Unicode编码
-   Java编程风格
    -   方法名: 多是动词,首字母小写,其于各单词首字母大写
    -   常量名: 字母全部大写,单词之间用下划线分隔

### 基本数据类型

Java数据类型分为两大类: 基本数据类型(整型(byte)、浮点型、字符型、布尔型)和复合数据类型(数组: 它是对象,而不是类、类和接口)

以0开头是八进制数

### 表达式

由运算符和操作数组成,对操作数进行运算符指定的操作,得出结果

**操作数**

-   常量
-   变量
    -   方法内定义的变量称为自动变量或局部变量
    -   类中定义的变量叫做成员变量
    -   简单数据类型在变量声明后,系统自动在内存分配相应的存储空间.说明引用后,系统只分配引用空间,程序员需要用new来创建对象实例,才会分配相应的存储空间
    -   java程序中不允许将未经初始化的变量用作操作数
    -   '\\\u0000' null
    -   变量作用域
        -   成员变量的作用域是整个类
        -   局部变量的作用域是从该变量的声明处到包含该声明的语句块结束处
        -   同一个类中的局部变量会屏蔽其同名的成员变量
        -   局部变量不能同名,会引起编译错误

**运算符**

-   算术运算符: 加、减、乘、除、取模
-   关系运算符: 大于、小于、等于...
-   逻辑运算符
    -   逻辑与、逻辑或、逻辑非
    -   短路: 进行运算时、先计算运算符左侧表达式的值、当使用该值能得到整个表达式的值,则跳过运算算右侧的表达式
-   位运算符
    -   按位取反\~,按位与,按位或，按位异或，右移、左移(<<)，无符号右移(>>>)
    -   正数:原码，反码，补码都一样，正数用原码表示
    -   负数:原码的最高位是符号位，反码是原码除符号位取反，补码是反码+1，负数用补码表示
    -   负数算术右移高位补1，正数则高位补0
-   扩展赋值运算符

# 第三章: 流程控制语句 

### Java程序的结构

一个Java程序可以由一个或多个.java文件组成，这些文件称为源文件。每个源文件中含有一个或多个类或接口

一个源文件中如果有多个类，则最多只能有一个公有类，且该源文件的名字即为这个公有类的名字，且大小写也要一致。其他非public的类的个数不限

Java程序的结构包含以下内容

-   package语句：包语句，每个文件最多只有一个，且必须放在文件开始的地方
-   import语句：引入语句，可以没有，也可以有多个，如果有import语句的话，必须放在所有类定义的前面
-   具有public权限的类定义：每个文件中最多有一个
-   类定义：每个文件中包含的非public权限的类定义的个数没有限制
-   接口定义：每个文件中包含的接口定义个数没有限制

Java包的概念

-   包是类的容器，包的设计人员利用包来划分名字空间，以避免类名冲突
-   自定义包: package pkgl \[. pkg2\[. pkg3...]]
-   一个文件中最多只能有一条package语句
-   包的名字有层次关系，各层之间以点分隔
-   通常包名中全部用小写字母
-   一个包要放在指定目录下，通常用CLASSPATH指定搜寻包的路径
-   类名就是文件名，包名就是文件夹名，即目录名

### 流程控制

概念

-   赋值语句：表达式可以当作一个值赋给某个变量，这样的语句称为赋值语句
-   表达式语句：有的表达式也可单独当作语句，这样的语句称为表达式语句

<!---->

-   if .. else
-   for
-   while
-   do while
-   break
    -   break语句的第三种使用方法是在块中和标号配合使用，语法格式:  break  标号;
        其语义是跳出标号所标记的语句块，继续执行后面的语句。这种形式的break语句多用于嵌套块中，控制从内层块跳到外层块之后
-   continue
    -   continue语句也可以和标号一起使用,语法格式:  continue 标号
        它立即结束标号标记的那重循环的当次执行，开始下一次循环。这种形式的语句多用于多重循环中

### 简单的输入/输出

**Scanner类**

-   Scanner类属于java.util包。它提供了许多方法，可用来方便地读入不同类型的输入值。比如从键盘输入、从文件中输入等
-   创建一个Scanner类对象，它读入键盘输入：
    Scanner scan = new Scanner(System.in)
-   方法
    -   next 方法读入下一个输入对象，将它作为字符串返回
    -   nextLine 读入当前行的所有输入，直到行尾，然后作为字符串返回

**NumberFormat类**

-   提供对数值进行格式化操作的一般功能, 定义在java.text包中
-   静态类
-   静态方法
    -   getlnstance():返回当前默认语言环境的默认数值格式
    -   getCurrencyInstance():返回当前默认语言环境的通用格式
    -   getNumberInstance():返回当前默认语言环境的通用数值格式
    -   getPercentInstance():返回当前默认语言环境的百分比格式
    -   setMaximumFractionDigits(int):设置数值的小数部分允许的最大位数

**DecimalFormat类**

-   对浮点数进度精度格式化, 定义在java.text包中
-   format(double): 一个具体的值进行格式化
-   applyPattern(): 改变对象要使用的模式

### 处理异常

**术语**

在一个方法的运行过程中，如果发生了异常，称程序产生了一个异常事件，相应地生成异常对象

生成异常对象并把它提交给运行时系统的这一过程称为抛出（Throw) —个异常

Java运行时系统从生成对象的代码块开始进行回溯，沿方法的调用栈逐层回溯，寻找相应的处理代码，直到找到包含相应异常处理的方法为止，并把异常对象交给该方法处理。这一过程称为捕获（Catch)

当发现并响应异常时，就是处理（Handle) 了异常

**异常分类**

异常类:Exception类是所有异常类的父类

-   受检异常(必须被处理): 是程序执行期间发生的严重事件的后果。
    发生的原因可能是用户给程序提供了一个错误的文件名
-   下列类表示受检异常类: ClassNotFoundException、FileNotFoundException、IOException、NoSuchMethodException、WriteAbortedException
-   运行时异常(不需要处理): 通常是程序中逻辑错误的结果,除以0
-   下列类表示受检异常类: ArraylndexOutOfBoundsException、ClassCastException、EmptyStackException、IndexOutOfBoundsException、IndexOutOfBoundsException、NullPointerException

错误类: Error类是所有错误类的父类,错误(不需要处理)例如发生了不正确的情况，如内存溢出可能引发受检异常的方法: 在方法内处理异常,告诉方法的调用者来处理。

# 第四章: 面向对象程序设计

### 类和对象

类的定义: 也称为类的声明。类中含有两部分元素，分别是数据成员变量和成员方法

可见性: 红框是与c#不同的地方

| 类型       | 无修饰符 | private | protected | public |
| -------- | ---- | ------- | --------- | ------ |
| 同一类      | 是    | 是       | 是         | 是      |
| 同一包中的子类  | 是    | 否       | 是         | 是      |
| 同一包中的非子类 | 是    | 否       | 是         | 是      |
| 不同包中的子类  | 否    | 否       | 是         | 是      |
| 不同包中的非子类 | 否    | 否       | 否         | 是      |

构造方法

1.  默认的构造方法
2.  构造方法重载

this引用

方法的定义

按值传送

1.  传给方法的值称为实参
2.  方法的参数列表中列出的值称为形参
3.  如果形参是基本数据类型的
4.  如果形参是引用

重载方法名: 允许多个方法使用同一个方法名，这就是方法名的重载: 与c#相同

静态成员：又称类成员，在类的定义中定义的一种特殊的成员，用static修饰，静态成员是不依赖于特定对象的内容。包括静态变量和静态方法,只在类定义时为静态成员分配内存，此时还没有创建对象，也没有对对象进行实例化

静态变量: 也被称为类变量，将一个变量定义为静态变量的方法就是将这个变量标记上关键字static

静态方法: 或称类方法，如果需要在尚未创建一个对象实例的时候就去引用方法的程序代码， 那么标记上关键字static即可实现,静态方法不能被重写。也就是说，在这个类的后代类中，不能有相同名称、相同参数列表的方法

### 包装类

概念: Java要管理的数据仅有两类，即基本数据类型值及对象引用想用处理对象一样的方式来处理基本类型的数据时，必须将基本类型值“包装”为一个对象,每种基本数据类型对应的包装类(java.long)。

| 基本数据类型 | 包装类     | 基本数据类型  | 包装类       |
| ------ | ------- | ------- | --------- |
| byte   | Byte    | double  | Double    |
| short  | Short   | char    | Character |
| int    | lnteger | boolean | Boolean   |
| long   | Long    | void    | Void      |
| float  | Float   |         |           |

和其他的包装类不一样的是，Void类不能被实例化，只表示void引用的概念

Integer类中的几个方法(其他的包装类有类似的方法）

1.  Integer( int value）：构造方法，创建Integer对象，用来保存值value
2.  byte byteValue ( )、double doubleValue ( ) 、 float floatValue ()、int intValue ( )、long longValue( )：按各自对应的基本数据类型返回Integer对象的值
3.  static intparseInt(String str)：按int类型返回存储在指定字符串str中的值
4.  static String toBinaryString (int num) 、static String toHexString (int num) 、static StringtoOctalString(int num)：将指定的整型值在对应的进制下按字符串形式返回

自动装箱: 自动将基本数据类型转换为对应的包装类的过程称为自动装箱

# 第五章: 数组和字符串

### 数组

一维数组

1.  类型\[ ] 数组名: int \[ ] intArray
2.  类型 数组名\[]: int intArray\[ ]
3.  静态初始化: int intArray\[ ] ={1, 2, 3, 4}
4.  动态初始化: String names \[ ]; names = new String\[4];

二维数组

1.  类型 数组名\[ ]\[ ]: int intArray\[ ]\[ ]
2.  类型\[ ]\[ ] 数组名
3.  类型\[ ] 数组名\[ ]
4.  静态初始化: int intArray\[ ]\[ ] = {{12，3}，{1，5}，{3，4}} ;
5.  动态初始化: int a\[ ] \[ ] =new int\[2] \[3]
6.  按维分配: 必须从最高维开始。类型 数组名\[]\[] = new类型\[数组第一维大小]\[];数组名\[0] = new类型\[数组第二维大小]; 数组名\[1]= new类型\[数组第二维大小]

### 字符串

在java.lang包中

String类用于处理不变字符串

1.  length()：返回字符串的长度，即字符个数
2.  charAt( int index)：返回字符串中index位置的字符
3.  subString(int beginlndex)：截取当前字符串中从beginlndex开始到末尾的子串
4.  replace ( char oldChar，char newChar )：将当前字符串中出现的所有oldChar转换为newChar
5.  toLowerCase()：将当前字符串中所有字符转换为小写形式
6.  concat( String str)：将str连接在当前字符串的尾部
7.  startsWith(String prefix)：测试prefix是否是当前字符串的前缀
8.  valueOf( type value)：将type类型的参数value转换为字符串形式
9.  String类型字符串的连接还可以使用运算符+来实现

StringBuffer类用于处理可变字符串

1.  length()：返回字符串的长度，即字符个数
2.  charAt( int index)：返回字符串中index位置的字符
3.  subString(int beginlndex)：截取当前字符串中从beginlndex开始到末尾的子串
4.  append( String str)：将参数str表示的字符串添加到当前串的最后
5.  replace( int start, intend, String str)：使用给定的str替换从start到end之间的子串
6.  capacity()：返回当前的容量。即字符串长度再加上缓冲区的大小（16）

字符串常量: 是用双引号括起来的一串字符。系统为程序中出现的字符串常量自动创建一个String对象，创建过程是隐含的

字符串变量: 在使用之前要显式声明，并进行初始化。方法

1.  compareTo( )
2.  equals( )
3.  equalsIgnoreCase( )
4.  regionMatched( )&#x20;
5.  \==: 判定两个字符串对象是否是同一实例，即它们在内存中的存储空间是否相同
6.  String substring(int beginIndex)
7.  String substring(int beginIndex, int endIndex)

### Vector类

java.util包

变长数组

保存的元素的类型可以不一样

Vector类的实例中只能保存对象类型，而不能是基本数据类型，例如int类型

成员变量

1.  protected intcapacityIncrement：增量的大小。如果值为0，则缓冲区的大小每次倍增
2.  protected intelementCount：Vector对象中元素的数量
3.  protected ObjectelementData\[ ]：元素存储的数组缓冲区
4.  capacity: 实例的容量
5.  elementCount: 实际保存的元素个数

构造方法: public Vector(int initialCapacity, int capacitylncrement)：以指定的初始存储容量initiaCapacity和容量增量capacityIncrement构造一个空的向量Vector

方法

1.  addElement(Object obj)：将新元素obj添加到序列尾部
2.  insertElementAt( Object obj，int index)：将指定对象 obj 插入到指定位置index处
3.  setElementAt(Object obj，int index)
4.  add( int index, Object obj)：在向量的指定位置index插入指定的元素obj
5.  removeElement(Objectobj)
6.  removeElementAt(int index)
7.  removeAllElements( )
8.  elementAt( int index)：返回指定位置处的元素
9.  contains (Object obj)：检查向量序列中是否包含指定的对象元素obj
10. indexOf (Object obj，int start\_index)：从指定的 start\_index 位置开始向后搜索，返回所找到的第一个与指定对象obj相同的元素的下标位置
11. lastIndexOf(Object obj, int start\_index)

# 第六章: 继承和多态

### 子类

子类与父类的关系是：子类对象“is a”（或“is kind of”）父类对象

如果一个类的定义中没有出现extends关键字，则表明这个类派生于Object类

Object类是Java程序中所有类的直接或间接父类，处在类层次的最高点

Object类方法

-   public final Class getClass()：获取当前对象所属的类信息，返回Class对象
-   public String toString()：按字符串对象返回当前对象本身的有关信息
-   public boolean equals(Object obj)：比较两个对象是否是同一个对象，是则返回true

多重继承的能力通过接口来实现

通过instanceof可以判定它的真正类型

### 方法覆盖与多态

方法覆盖(方法重写或隐藏)：父类中原有的方法可能不能满足新的要求，因此需要修改父类中已有的方法;子类方法不能比父类方法的访问权限更严格。

重载: 方法名相同，而参数列表不同

子类中还想使用父类中被隐藏的方法，可以使用super关键字

super的调用必须放在子类开头位置

多态

-   重载一个方法名
-   父子类之间直接或间接重写的方法名要由对象在运行时确定将调用哪个方法

动态绑定：或称后绑定，调用稍后可能被覆盖的方法的这种处理方式

静态绑定：或称前绑定，在编译过程中能确定调用方法的处理方式

### 终极类与抽象类

关键字final：表示终极，既可以修饰一个类，也可以修饰类中的成员变量或成员方法

一个类被定义为final，则它不能有子类

如果一个方法被定义为final，则不能被覆盖

如果一个变量被定义为final，则它的值不能被改变(常量)

关键字abstract：表示抽象，它可以用于类或方法

使用abstract修饰的方法的方法体为空，修饰的类必须被子类继承

### 接口

一个“纯”的抽象类: \[接口修饰符] interface  接口名 \[extends父接口列表]

Java允许一个类实现多个接口，从而实现了多重继承的能力

接口的实现: public class 类名 implements 接口名\[，接口名\[，接口名]]

在接口中定义的成员变量都默认为终极静态变量

# 第七章: 输入和输出流

### 数据流基本概念

输入数据流: 只能读不能写的数据流

java.io包中所有输入数据流都是从InputStream抽象类继承

方法

-   int read(): 从输入数据流中读取一个字节的二进制数据
-   int read(byte\[]): 将多个字节读到数组中,填满整个数组
-   int read(byte\[]b, int off, int len): 读到len长数据,从b数组中的off下标位置开始存
-   void close(): 关闭数据流
-   int available(): 返回目前可以从数据流中读取的字节数
-   long skip(long l): 跳过数据流中指定数量的字节不读取,返回实际跳过字节数
-   boolean markSuppert(): 是否支持回推操作
-   void mark(int markarea) 用于标记当前数据流位置 
-   void reset(): 将输入流重新定位到对此数据流最后调用mark的位置

输出数据流: 只能写不能读的数据流

java.io包中所有输入数据流都是从OutputStream抽象类继承

方法

-   void write(int i): 将字节i写到数据流中,但只写整型i的低8位
-   void write(byte b\[]): 将数组b\[]中的全部b.length个字节写入数据流
-   void write(byte b\[], int off, int len): 将数组b\[]中从下标off开始的len个字节写入数据流
-   void close(): 当结束对输出数据流的操作时应该将其关闭
-   void flush(): 刷新此输出流并强制写出所有缓冲的输出字节

Reader抽象类

Writer抽象类

### 基本字节数据流

文件输入流

FileInputStream=new FileInputStream("filename")

FileOutputStream = new FileOutputStream("filename")

缓冲区数据流

-   BufferedInputStream
-   BufferedOutputStream

数据数据流

DataInputStream t=new DataInputStream(is)

readUTF()

readByte()

readLong()

DataOutputStream t=new DataOutputStream(os)

对象流

ObjectInputStream

ObjectOutputStream os = new ObjectOutputStream(FileOutputStream f)

writeObject(object)

序列化: 能够记录自已的状态以便将来得到复原的能力,称为对象的持久性.

ObjectInputStream

ObjectOutputStream

基本字符流

# 第八章: 图形界面设计

### AWT和Swing

多数Swing组件以字母"J"开头, AWT组件与Swing组件最大的不同是Swing组件在实现时不包含任何本地代码

### 容器

分容器组件和非容器组件。有些容器可以嵌套，在这个嵌套层次的最外层，必须是一个顶层容器

顶层容器: JFrame,JApplet,JDialog,JWindow

public void setLayout(LayoutManager manager): 设置布局管理器

public setSize(int w, int h): 设置大小

内容窗格: Container

-   JPanel getContentPane(): 获取Panel
-   void setContentPane(JPanel panel): 设置Panel
-   setBackground(Color): 设置背景颜色 

普通面板: JPanel

-   new JPanel(): 创建FlowLayout实例
-   new JPanel(LayoutManager layout): 创建指定布局管理器实例
-   setBackground(Color): 设置背景颜色 
-   add(): 添加组件

滚动面板: JScrollPane

-   new  JScrollPane(): 创建一个空的JScrollPane
-   new  JScrollPane(Component view): 创建一个显示指定组件内容的JScrollPane,只要组件的内容超过视图大小,就会显示水平和垂直滚动条
-   void setHorizontalScrollBarPolicy(int policy): 确定水平滚动条何时显示在滚动窗格上,参数policy的可选值下列三者之一

### 标签及按钮

标签(JLabel)

-   new JLabel(): 创建一个即不显示文本又不显示图标的空标签
-   new JLabel(String text): 创建一个显示文本标签
-   new JLabel(String text, int horizontalAlignment): 创建一个显示文本标签及水平对齐方式
-   new JLabel(Icon image): 创建一个显示图标的标签
-   new JLabel(Icon image,  int horizontalAlignment): 创建一个显示图标的标签及水平对齐方式
-   new JLabel(String text, Icon image,  int horizontalAlignment): 创建一个显示文本和显示图标标签及水平对齐方式
-   setHorizontalAlignment(JLabel.CENTER): 设置水平对齐方式
-   setVerticalAlignment(JLabel.CENTER): 设置垂直对齐方式

按钮(JButton)

-   new JButton(): 创建一个即没有显示文本又没有图标的按钮
-   new JButton(Icon icon): 创建一个即没有显示文本但显图标的按钮
-   new JButton(String text, Icon icon): 创建一个显示文本和图标的按钮
-   临听事件: 类继承ActionListener接口,且用AddActionListener(this)方法注册事件
-   public void  setMnemonic(int mnemonic): 设置当前按钮的键盘助记符
-   public void setText(String text): 设置按钮的文本
-   public String getText(): 获取按钮的文本
-   public void  setToolTipText(String text); 设置显示的提示文本
-   public void addActionListener(ActionListener l): 为按钮添加事件侦听程序

切换按钮(JToggleButton)

-   new JToggleButton()创建一个即没有显示文本又没有图标的切换按钮
-   new JToggleButton(Icon icon)创建一个有图标的切换按钮
-   new JToggleButton(Icon icon, boolean selected)创建一个有图标和可设置初始状态的切换按钮
-   new JToggleButton(String text)创建一个显示文本的切换按钮
-   new JToggleButton(String text, boolean selected)创建一个显示文本和可设置初始状态的切换按钮
-   new JToggleButton(String text, Icon icon)创建一个显示文本和图标的切换按钮
-   new JToggleButton(String text, Icon icon, boolean selected)创建一个显示文本和图标和可设置初始状态的切换按钮

复选按钮(JCheckBox)

单选按钮(JRadioButton)

### 布局管理器

java.awt.FlowLayout: 将组件逐个放置在容器的一行上超过一行就超新行

-   new FlowLayout(): 创建一个默认的FlowLayout布局管理器,居中对齐,默认的水平和垂直间距是5个像素
-   new FlowLayout(int align): 创建一个默认的FlowLayout布局管理器,指定水平对齐方式,默认的水平和垂直间距是5个像素
    例: new FlowLayout(FlowLayout.LEFT)
-   new FlowLayout(int align, int hgap, int vgap): 创建一个默认的FlowLayout布局管理器,指定水平和垂直对齐方式,默认的水平和垂直间距是5个像素
-   例: frame.getContentPane().setLayout(new FlowLayout())

java.awt.BorderLayout(默认): 分五个区域North: 上部、South: 下部、West: 左部、East:右部、Center:中心

-   new BorderLayout()
-   new BorderLayout(int hgap, int vgap)
-   例: frame.getContentPane().add(button, BorderLayout.SOUTH)

java.awt.GridLayout: 网格式布局:将空间分成若干行乘若干列组件依次放入,每个组件占一格子

-   new GridLayout(): 创建只有一行的网格,网格列数根据实际需要而定
-   new GridLayout(int rows, int cols)
-   new GridLayout(int rows, int cols, int hgap, int vgap): 创建指定行数和列数以及行间距和列间距
-   例: frame.getContentPane().setLayout(new GridLayout(3, 2))

java.awt.CardLayout: 卡片式的管理器,一次只显示一项(选项卡)

-   new CardLayout(): 创建一个默认的无间距的新的CardLayout布局管理器
-   new CardLayout(int hgap, int vgap)
-   public void first(Container parent): 翻转到容器的第一张卡片
-   public void last(Container parent): 翻转到容器的最后一张卡片
-   public void next(Container parent): 翻转到容器的下一张卡片
-   public void prev(Container parent): 翻转到容器的上一张卡片
-   public void show(Container parent, String name): 翻转到容器的指定名字的卡片上

java.swing.BoxLayout: 将容器中的组件按水平或垂直排成一行,行排宽度可调,垂直高度可排

-   new BoxLayout(Container target, int axis): 创建一个将沿给定轴放置组件的布局管理器
-   BoxLayout.X\_AXIS: 水平
-   BoxLayout.Y\_AXIS: 垂直

空布局

-   setBounds(int x, int y, int width, int height)
-   例: JButton b1 = new JButton("Yes");
    b1.setBounds(60, 60, 75, 50);

### 事件处理

事件处理模型

-   public void addActionListener(ActionListener l): 注册事件侦听程序
-   public void removeActionListener(ActionListener l): 删除事件侦听程序

事件的种类

事件适配器

### 绘图基础

颜色

-   Color.black: 黑色
-   Color.blue: 蓝色
-   Color.cyan: 青色
-   Color.darkGray: 深灰色
-   Color.lightGray: 浅灰色
-   Color.green: 绿色
-   Color.magenta: 洋红色
-   Color.orange: 橙色
-   Color.pink: 粉红色
-   Color.red: 红色
-   Color.white: 白色
-   Color.yellow: 黄色
-   public void setForeground(Color c): 设置前景色
-   public void setBackground(Color c): 设置背景色

字体

-   public void drawChars(char\[]data, int offset, int length, int x, int y): 使用此图形上下文的当前字体和颜色显示字符数组data中从offset位置开始、最多length个字符,首字符的基线位于此图形上下文坐标系统的(x, y)处
-   public void drawString(String aString, int x, int y): 在指定位置显示字符串aString
-   public void drawBytes(char\[] data, int offset, int length, int x, int y): 使用此图形上下文的当前字体和颜色显示由指定的byte数组data中从offset位置开始、最多length个字符。首字符的基线位于此图形上下文坐标系统的(x, y)处
-   new Font(String name, int style, int size); 根据指定名称、样式和字号,创建一个新Font
    例: Font f = new Font("Dialog", Font.PLAIN, 14);
    -   String getName(): 返回此Font的字体名称
    -   int getSize(): 返回此Font的字号大小，舍入为整数
    -   int getStyle(): 返回此Font的样式
    -   boolean isBold(): Font对象的样式是否为BOLD
    -   boolean isItalic(): Font对象的样式是否为ITALIC
    -   boolean isPlain(): Font对象的样式是否为PLAIN

java.awt.Graphics类的基本功能

建立字体、设定显示颜色、显示图像和文本、绘制和填充各种几何图形

设置绘图模式

setPaintMode(): 将此图形上下文的绘图模式设置为正常模式,默认模式

setXORMosw(Color c): 将此图形上下文的绘图模式设置为异或模式,参数c指定了绘制对象时与窗口进行异或操作的颜色

应重写paintComponent(Graphics g)绘制组件的方法

1.  drawArc(int x, int y, int width, int height, int startAngle, int arcAngle);沿着由左上角为(x, y),宽高(width, height)的外接矩形所限定的椭圆绘制一条弧.弧起始于startAngle,延伸的距离由的距离sarcAngle所定义
    fillArc(int x, int y, int width, int height, int startAngle, int arcAngle)
2.  drawLine(int x1, int y1, int x2, int y2): 绘制一条从点(x1, y1)到点(x2, y2)的直线
    fillLine(int x1, int y1, int x2, int y2)
3.  drawOval(int x, int y, int width, int height): 绘制一个由左上角为(x, y)、宽为width、高为height的外接矩形所限定的椭圆fillOval(int x, int y, int width, int height)
4.  drawPolygon(int\[] xPoints, int\[] yPonts, int nPoints): 绘制x和y坐标数组定义的一系列连接线。每对(x, y)坐标定义了一个点。如果第一点和最后一个点不同,则图形不是闭合的
    fillPolygon(int\[] xPoints, int\[] yPonts, int nPoints)
5.  drawRect(int x, int y, int width, int height): 绘制一个矩形,其左上角为(x, y),宽为width, 高为height
    fillRect(int x, int y, int width, int height)
6.  drawRoundRect(int x, int y, int width, int height, int arcWidth, int arcHeight):  用此图形上下文的当前颜色绘制圆角矩形的过程。矩形的左边和右边分别位于x和x+width。矩形的顶边和底边位于y和y+height
    fillRoundRect(int x, int y, int width, int height, int arcWidth, int arcHeight)
7.  drawString(String str, int x, int y): 在点(x, y)处输出字符串str,向右扩展
8.  draw3DRect(int x, int y, int width, int height, boolean raised): 绘制指定矩形的3D突出显示边框。矩形边框的左上角为(x, y),宽为width,高为height, raised提示矩形是凸出平面显示还是凹入平面显示

Graphics2D绘图

图形状态属性

-   stroke: 控制线的宽度、笔形样式、线段连接方或划线图案
    创建线BasicStorke对象后,再调用setStroke()方法即设置stroke属性
    BasicStroke(float w): 指定线的宽度w
    BasicStorke(float w, int cap, int join); 指定线的的宽度w,端点样式cap及两线段交汇的连接样式
-   paint属性: 控制填充效果。先调用GradientPaint()方法确定填充效果。再使用setPaint()方法进行设置.
    GradientPaint(float x1, float x2,  Color2 c1, float y1, float y2, Color2 c2): 构造一个简单的非周期性的GradientPaint对象。从点A(x1, y1)到点B(x2, y2), c1是点A处的颜色, c2是点B处颜色, 从c1渐变到c2
-   transform属性: 该属性用来实现常用的图形位移、缩放和斜切等变换操作.首先创建AffineTransform对象,然后调用setTransform()方法设置transform属性。最后,使用具有指定属性的Graphics2D对象绘制图形
    AffineTransform(): 构造一个表示仿射(Identity)变换新的AffineTransform
    getRotateInstance(double theta): 旋转theta弧度
    getRotateInstance(double theta, double x, doube y): 绕旋转中心(x, y)旋转
    getScaleInstance(double sx, double sy): x和y方向按sx, sy比例变换
    getTranslateInstance(double tx, double ty): 平移变换
    getShearInstance(double shx, double shy): 斜切变换,shx和shy指定斜拉度

绘图方法

-   java.awt.geom包中几何图形类Line2D线段类、RoundRectangle2D圆角矩形类、Ellipse2D椭圆类、Arc2D圆弧类、QuadCurve2D二次曲线类和CubicCurve2D三次曲线类
-   Graphics2D画一个图形的步骤: 首先重画方法paintComponent()或paint()中,把参数对象强制转换成Graphics2D对象;然后,用上述各图形类提供的静态方法Double()创建该图形的对象;最后,以图形对象为参数调用Graphics2D对象的draw()方法绘制这个图形也可以先用java.awt.geom包提供的Shape对象,并用单精度Float坐标或双精度Double坐标创建Shape对象,然后再调用draw()方法进行绘制

几何图形类

-   Line2D line = new Line2D.Double(2, 3, 200, 300); 起点(3, 2),终点(200, 300)
-   Rectangle2D rect = new Rectangle2D.Double(20, 30, 80, 40); 矩形的左上角(20, 30), 宽高(80，40)
-   RoundRectangle2D rectRound = new RoundRectangle.Double(20, 30, 130, 100, 18, 15); 声明并创建圆角矩角,左上角(20, 30)宽高(130, 100), 长轴18,短轴15
-   Ellipse2D ellipse = new Ellipse.Double(20, 30, 100, 50);声明并创建椭圆,左上角(20, 30),宽是100,高是50
-   Arc2D arc1 = new Arc2D.Double(8, 30, 85, 60, 5, 90, Arc2D.OPEN); 声明并创建圆弧,外接矩形的左上角是(8, 30), 宽是85,高是60,超始角是5度,终止角是90度,Arc2D.OPEN表示一个开弧, Arc2D.CHORD 弓弧和Arc2D.PIE饼弧
-   二次曲线: y(x) = ax^2+bx+c
    QuandCurve2D curve1 = new QuadCurver2D.Double(20, 10, 90, 65, 55, 155);
    起始点(20, 10) 控制点(90, 65) 终点(55, 155)
-   三次曲线: y(x) = ax^3 + bx^2 + d
    CubicCurve2D curve1 = new  CubicCurve2D(12, 30, 50, 75, 15, 15, 115, 93);
    起始点, 两个控制点,和终点

# 第九章: Swing组件

组合框(JComboBox):是一个下拉式菜单,它有两种形式可编辑和不可编辑的,对于可编辑的即可从下拉菜单中选择,又可以输入新的内容

方法:

1.  void addItem(Object anObject); 在末尾位置添加新的可选项
2.  Object getItemAt(int index); 返回指定索引序号index处可选项
3.  int getItemCount(); 返回项的数目
4.  void insertItemAt(Ojbect obj, int index); 在指定位置插入新的可选项
5.  int getSelectedIndex(): 返回列表中与给定项匹配的第一个选项的索引序号
6.  Object getSelectedItem(): 返回当前所选项
7.  void removeAllItem(): 删除所有项
8.  void removeItem(Object obj); 删除某一项
9.  void removeItemAt(int anIndex): 删除指定索引项

### 列表(JList):&#x20;

是可供用户进行选择的一系列可选项

new JList():构造一个空列表new JList(Object\[] listData): 构造一个列表,列表的可选项由对象数组listData指定new JList(Vector\<?> listData): 构造一个列表,使其显示Vector中的元素

当用户在列表上进行选择时触发ListSelectionEvent事件,JList提供了一个addListSelectionListener(ListSelectioner listener)方法注册侦听事件, 在ListSelectionListener接口中只包含一个方法
public void valueChanage(ListSelectionEvent e);

列表即支持单项选择又支持多项选择,用JList中定义的setSelectionMode(int selectMode):

方法定义:

-   ListSelectionModel.SINGLE\_SELECTION: 只能进行单项选择
-   ListSelectionModel.SINGLE\_INTERVAL\_SELECTION: 连接的多项选择
-   ListSelectionModel.MULTIPLE\_INTERVAL\_SELECTION: 默认项, 可多项目选择,项之间也可以是间断的

文件组件父类(JTextComponent): 是文本域(JTextField),口令输入域(JTextPasswordFiled), 文件区(JTextArea)的父类

-   String getSelectedText(): 从文件组件中提取选中的内容
-   String getText(): 提取所有内容
-   String getText(int offs, int len): 指定范围内提取内容
-   void select(int selectionStart, int selectEnd): 提取起始和结束位置内容
-   void selectAll(): 在文本组件中选中所有文本内容
-   void setEditable(boolean b): 设置为可编辑或不可编辑状态 
-   void setText(String t): 设置文本组件中的文本内容
-   void setDocument(Document doc): 设置文本组件的文档
-   void copy(): 复制选中的文本到剪贴板
-   void cut(): 剪切选中的文本到剪贴板
-   void paste(): 将剪贴版的内容粘贴到当前位置
-   public boolean requestFocusInWindow(): 请求当前组件获得焦点

### 文本域(JTextField)

单行的文本输入框,可用于输入少量文本

常用构造方法:

-   new JTextField(); 空文本域
-   new JTextField(int columns); 指定列数的空文本域
-   new JTextField(String text); 显示初始字符串的文本域
-   new JTextField(String text, int columns);&#x20;

常用方法:

-   void addActionListener(ActionListener l): 添加指定的操作侦听器,接收操作事件
-   void removeActionListener(ActionListener l): 移除指定的操作侦听器,不再接收操作事件
-   void setFont(Font f): 设置当前字体
-   void setHorizontalAlignment(int alignment): 设置文本的水平对齐方式.有效值包括JTextField.LEFT, JTextField.RIGHT, JTextField.CENTER, JTextField.LEADING, JTextField.TRAILING
-   int getColumns(): 返回文本域列数

### 文本区(JTextArea)

文本区是一个多行多列的文本输入框

构造方法:

-   new JTextArea(); 构造一个空文本区
-   new JTextArea(String text); 显示初始字符串的文本区
-   new JTextArea(int rows, int columns); 构造一个具有指定行数和列数的空文本区
-   new JTextArea(String text, int rows, int columns);&#x20;

常用方法:

-   void append(String str); 将指定文本str插入到文本区的特定位置
-   void insert(String str, int pos);  将指定文本str插入文本区的pos位置处
-   void replaceRange(String str, int start, int end); 用指定文本str替换文本区中从起始位置start到结尾end的内容

### 菜单栏及菜单

包括JMenuBar、JMenuItem、JMenu、JCheckBoxMenuItem、JRadioButtonMenuItem和JPopupMenu等

菜单栏是窗口中的主菜单,用来包容一组菜单

JMenu菜单:

-   new JMenu(); 构造没有文本的新菜单
-   new JMenu(String s); 构造具有指定标签的带有初始文本新菜单
-   new JMenu(String s, boolean b); 构造具有指定标签的带有初始文本新菜单, b表示是否可以分离
-   addSeparator();添加分隔项

### 菜单项(JMenuItem)

-   new JMenuItem(); 创建不带有设置文本或图标的菜单项
-   new JMenuItem(Icon icon); 创建一个只显示图标的菜单项, 图标由Icon型参数icon指定.
-   new JMenuItem(String text); 创建一个只显示文本的菜单项,文本由String型参数text指定
-   new JMenuItem(String text, Icon icon); 创建一个同时显示文本和图标的菜单项,文本由String型参数text指定,图标由Icon型参数icon指定
-   new JMenuItem(String text, int mnemonic); 创建一个显示文本并且有快键菜单项,文本由String型参数text指定,快捷键由int型参数mnemonic指定

### 复选菜单项(JCheckBoxMenuItem)

-   new JCheckBoxMenuItem(); 创建一个未设置文本或图标、最初也未选定复选框菜单项
-   new JCheckBoxMenuItem(Icon icon); 创建一个有图标、最初未被选定的复选框菜单项
-   new JCheckBoxMenuItem(String text); 创建一个带文本,最初末被选定的复选框菜单项
-   new JCheckBoxMenuItem(String text, boolean b); 创建一个带文本和选择状态的复选框菜单项
-   new JCheckBoxMenuItem(String text, Icon icon, boolean b); 创建一个带文本、图标和选择状态的复选框菜单项

### 单选菜单项(JRadioButtonMenuItem)

-   new JRadioButtonMenuItem(); 创建一个未设置文本或图标的单选按钮菜单项
-   new JRadioButtonMenuItem(Icon icon); 创建一个带图标的单选按钮菜单项
-   new JRadioButtonMenuItem(string text); 创建一个具有指定文本的单选按钮菜单项
-   new JRadioButtonMenuItem(string text, boolean selected); 创建一个具有指定文本和选择状态的单选按钮菜单项
-   new JRadioButtonMenuItem(string text,  Icon icon); 创建一个具有指定文本和图标的单选按钮菜单项
-   new JRadioButtonMenuItem(string text,  Icon icon, boolean selected); 创建一个具有指定文本、图标和选择状态的单选按钮菜单项

### 对话框(JDialog)

-   new JDialog(Dialog owner); 创建一个没有标题但将指定的对话框作为其所有者的无模式对话框
-   new JDialog(Dialog owner, boolean modal); 创建一个没有标题但将指定的对话框作为其所有者的对话框,modal指定对话框是有模式或无模式
-   new JDialog(Dialog owner, string title, boolean modal); 创建有标题但将指定的对话框作为其所有者的对话框,modal指定对话框是有模式或无模式
-   new JDialog(Frame owner); 创建一个没有标题但将指定的框架作为其所有者的无模式对话框
-   new JDialog(Frame owner, boolean modal); 创建一个没有标题但将指定的框架作为其所有者的对话框,modal指定对话框是有模式或无模式
-   new JDialog(Frame owner, string title, boolean modal); 创建一个有标题但将指定的框架作为其所有者的对话框,modal指定对话框是有模式或无模式

### 标准对话框(JOptionPane)

在类中定义了多个showXxxDialog形式的静态方法

-   showConfimDialog: 确定对话框,显示问题,要求用户进行确定
-   showInputDialog: 输入对话框,提示用户输入
-   showMessageDialog: 信息对话框,显示信息,告知用户发生了什么情况
-   showOptionDialog: 选项对话框,显示选项,要求用户进行选择

除了showOptionDialog之外,其它3种方法都定义有若干个不同格式的同名方法,例:

-   showMessageDialog(Component parentComponent, Object message);
-   showMessageDialog(Component parentComponent, Object message, String title, int messageType);
-   showMessageDialog(Component parentComponent, Object message, String title, int messageType, Icon icon);

Component parentComponent: 对话框的父窗口对象,其屏幕坐标将决定对话框的显示位置;此参数也可以为null,表示采用默认的Frame作为父窗口,此时对话框将设置在屏幕的正中

-   String title: 对话框的标题
-   Object message: 显示在对话框中的描述信息.该参数通常一个String 对象, 但也可以是一个图标,一个组件或对象数组
-   int messageType: 对话框所传递的信息类型
-   intoptionType: 对话框上按钮的类型,可以为以下变量
-   Object\[] options: 对话框上的选项,在输入对话框中,通常以组合框形式显示,在选项对话框中,则是指按钮的选项类型.该参数通常是一个String数组,也可以是图标或组件数组
-   Icon icon: 对话框上显示的装饰图标,如果没有指定,则根据messageType参数显示默认图标
-   Object initialValue: 初始选项或输入值

### 文件对话框(JFileChooser)

文件对话框是专用于对文件(或目录)进行浏览和选择的对话框

常用的构造方法:

1.  new JFileChooser(); 构造一个指向用户默认目录的文件对话框
2.  new JFileChosser(File currentDirectory); 使用给定的File作为路径来构造一个文件对话框
3.  new JFileChosser(String currentDirectoryPath); 使用给定的路径来构造一个文件对话框

刚刚创建的文件对话框是不可见的,可以用以下方法将其显示出来

1.  showOpenDialog(Component parent); 弹出一个"打开"文件对话框
2.  showSaveDialog(Component parent); 弹出一个"保存"文件对话框

当用户进行文件选择之后,可以通过getSelectedFile()方法取得用户所选择的文件

# 第十章: 多线程

### 线程和多线程

线程概念: 是进程执行过程中产生的多条执行线索,是比进程单位更小的执行单位,在形式与进程十分相似,不同的是它没有入口,也没有出口,因此其自身不能自动运行,百必须栖身某一个进程中

结构: 由三部分组成

1.  虚拟CPU,封装在java.lang.Thread类中,它控制整个线程的运行
2.  执行的代码,传递给thread类,由Thread类控制按序执行
3.  处理的数据,传递给thread类,是在代码执行过程中所要处理的数据

状态

-   新建: 线程对象刚刚创建,还没有启动,此时还处于不可运行状态,但已有了相应的内存空间以及其它资源
-   可运行状态: 此时线程已经启动,处于线程的run()方法之中, 调用start()方法可使线程处于运行状态
-   死亡: 线程死亡的原因有两个,一是run()方法中最后一个语句执行完毕,二是当线程遇到异常退出时便进入了死亡状态
-   阻塞: 一个正在执行的线程因特殊原因,被暂停执行,就进入阻塞状态。阻塞时线程不能进入就绪队列排队,必须等到引起阻塞的原因消除,才可以重新进入队列排队
    两个方法: sleep()和wiat()是两个常用的引起阻塞的方法
-   中断线程: 在程序中常常调用interrupt()来终止线程.interrupt()不仅可中断正在运行的线程,而且也能中断处于blocked状态的线程,此时interrupt()会抛出一个InterruptedException异常
    void interrupt():
    static boolean interrupt():
    boolean isInterrupt(): 检测当前线程是否已被中断,不改变interrupt值

### 创建线程

java.lang.Thread是java中用来表示线程的类,如果一个类定义为Thread的子类,那么这个类的对象就可以用来表示线程.

new Thread(ThreadGroup group, Runnable target, String name); name作为新线程的名称,且是线程组group中的一员,而target必须实现Runnable接口,它是另一个线程对象,当本线程启动时,将调用target的run()的方法;当target为null时,启动本线程的run()方法.

### 线程基本控制

线程的启动方法:

1.  start():启动线程,让线程从新建状态到就绪状态
2.  run(): 用来定义线程对象被调度之后所执行的操作,必须重写run方法
3.  yield(): 强制终止线程运行
4.  isAlive():测试当前线程是否在活动
5.  sleep(int millsecond): 睡眠
6.  void wait(): 等待

线程的调度:虽然线程已经处于就绪状态,但这并不意味着这个线程一定会被立刻运行在java中线程是抢占式,而不是时间片式。

优先级策略:

1.  优先级高的先执行,优先级低的后执行
2.  每个线程创建时都会被自动分配一个优先级,默认时,继承其父类的优先级
3.  任务紧急的线程,优先级较高
4.  同优先级的线程按'先进先出"的调度原则
5.  Thread类有3个与线程与关的静态变量
6.  MAX\_PRIORITY: 最高优先级,值为10
7.  MIN\_PRIORITY: 最低优先级,值为1
8.  NORMAL\_PROIORITY: 默认优先级,值为5

线程结束: interrupt();强制中断

挂起线程:

1.  sleep(): 暂时停止一个线程的执行
2.  wait(), notify(), notifyAll(): wait()方法使当前线程等待,直到其它线程调用此对象的notify或notifyAll()
3.  join(): 将引起现行线程等待,直到join()方法所调用线程结束

线程的互斥: 有时多个线程要共享数据但又要保持数据的一致性和正确性

对象互斥锁: 用关键字volatile声明一个共享变量有关键字synchronized来声明操作共享数据的一个方法或一段代码

线程的同步
