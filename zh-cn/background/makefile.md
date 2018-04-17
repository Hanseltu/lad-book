# Makefile

## 前言

在介绍Makefile之前，先来认识一下make。GNU make(简称make)是Linux环境下构建和管理自己工程的强有力工具。在Linux(Unix)下使用GNU的make工具能够比较容易构建任何一个工程，整个工程只需要一个命令就可以完成从编译、链接到最终执行的功能。make命令正常工作的基础就是Makefile文件。

Makefile文件描述了整个工程的编译、链接等相关规则。具体的规则包括：工程中哪些源文件需要编译以及如何编译，需要创建哪些库文件以及如何创建这些库文件，如何产生最终的可执行文件等等。尽管为整个工程编写一个Makefile文件可能会比较耗时，但是为工程提供一个正确的Makefile文件的优势是可以使用一个命令完成”自动化编译“过程，极大提高工程开发效率。

一个Makefile文件编写需要遵守一定的语法规则。其中包括Makefile的书写规则，变量使用规则，条件执行，make运行，make内嵌函数以及make的隐含规则。Linux 0.11内核中的Makefile文件仅使用到了Makefile的普遍规则，因此在本节只介绍Makefile的初级使用规则，更高级的使用规则请参考本小节末的参考文档。

## Makefile总述

### Makefile文件命名

默认情况下，make命令会在当前目录下按顺序找文件名为"GNUmakefile"、"makefile"、"Makefile"的文件，找到了则按照此文件的规则执行相关命令。在这三个文件名中，最好使用"Makefile"

这个文件名，这个文件名首字母大写，比较醒目。同时，也可以使用别的文件名来书写Makefile规则，比如"Make.Linux"、"Make.Solaris"、"Make.AIX"等，此时在执行make命令时需要指定需要

执行的Makefile，使用make的"-f"和"-file"参数即可，如`make -f Make.Linux`或`make -file Make.Linux`。

### Makefile的内容

Makefile中主要包括了五个部分，分别为显式规则、隐晦规则、变量定义、文件指示和注释。

* 显式规则

显式规则说明了如何生成一个或者多个目标文件。由Makefile文件编写者明确指出要生成的文件，文件之间的依赖关系以及生成文件的命令等。

* 隐晦规则

由于make具有自动推导的功能，隐晦规则允许Makefile文件编写者比较粗略地书写部分规则，这是make命令所支持的重要功能。

* 变量定义

在Makefile中允许定义一系列的变量，在Makefile中，变量一般都是字符串，与C语言中的宏定义有些类似。Makefile在被执行时，其中的变量都会被扩展到相应的应用位置上。

* 文件指示

文件指示包括了三个部分。第一部分，可以在一个Makefile中引用另一个Makefile，就像C语言中的include一样；第二部分是可以根据某些情况指定Makefile中的有效部分，就像C语言中的#if

一样；第三部分是可以定义一个多行的命令。

* 注释

Makefile中只有行注释


### Makefile中的变量



## Makefile的规则


### 规则语法

### 伪目标和多目标

### 静态模式

### 自动生成依赖性



## make的运行


### make的退出码

### 指定make目标

### 检查规则

### make的参数

## 参考

* **《GNU make中文手册》**

* **《跟我一起写Makefile-陈皓》**

* **《Linux内核完全注释-赵炯》**
