======================================================================================================================================================
Linux动态库接口函数/库或可执行程序依赖包查看
======================================================================================================================================================



ldd
    查看依赖


::

    [root@VM-24-4-centos lib]# ldd libjsoncpp.so.1.9.4
            linux-gate.so.1 =>  (0xf77ca000)
            libstdc++.so.6 => /lib/libstdc++.so.6 (0xf7693000)
            libm.so.6 => /lib/libm.so.6 (0xf7651000)
            libgcc_s.so.1 => /lib/libgcc_s.so.1 (0xf7636000)
            libc.so.6 => /lib/libc.so.6 (0xf746b000)
            /lib/ld-linux.so.2 (0xf77cb000)





nm
    列出这个SO库中的所有符号及其地址

::

    nm -gC xxx.so

-g
    表示显示全局符号
-C
    表示显示C++符号

nm输出第二列：

- T (text): 该符号位于代码段（text segment）中，通常是函数或方法的地址。
- D (data): 该符号位于数据段（data segment）中，通常是已初始化的全局或静态变量。
- B (bss): 该符号位于未初始化数据段（bss segment）中，通常是未初始化的全局或静态变量。
- U (undefined): 该符号在目标文件中未定义，但在其他地方（如另一个目标文件或库中）引用。这通常表示一个需要链接器解决的外部依赖。
- W (weak): 弱符号。链接器将首先解析非弱符号，然后才考虑弱符号。如果有多个定义，链接器将选择第一个找到的非弱定义。


objdump
    查看该函数的定义，使用objdump命令

::

    objdump -D xxx.so | grep 函数名


-D
    表示反汇编所有节(section)的内容，然后使用grep命令过滤出包含该函数名的内容。



readelf
    - 查看SO库函数
    - readelf是一个Linux系统下的ELF格式可执行文件的查看工具。ELF(Executable and Linkable Format)是Linux下二进制文件格式的标准，它包含了代码、数据和符号表等多种信息。

使用readelf命令查看SO库函数的方法：

::
    
    readelf -s xxx.so

-s
    表示显示符号表



