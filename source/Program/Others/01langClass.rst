.. _program_lang_class:

======================================================================================================================================================
语言分类
======================================================================================================================================================





高级语言和低级语言
======================================================================================================================================================

    低级语言：汇编语言、机器语言，嵌入式等；
        特点：特点是执行效率高，速度快；因为它们都是接近底层编程，没有编译解析等过程，程序直接操控硬件，效率相对较高，
        但是其学习和编程调试难度较高，编程比较慢，且比较费时，项目周期长。
    高级语言：c、c++、java、python、PHP、c#。
        特点：高级语言是依赖编译解析的，更接近于人类语言逻辑的编程语言，其可读性更高，开发效率更高，学习起来相对较容易；
        但是其执行效率较低级语言而言要低一些，而且高级语言的执行，需要依赖运行环境，
        在Java等编程语言中，如果环境配置不完善，或者环境版本不一致则可能导致程序无法执行。

    这个是很好识别的，低级语言更接近于机器指令，而高级语言更接近于人的一般的思维模式。
    高级语言大部分不能直接更硬件打交道，这使得程序相对于低级语言运行速度降低，但是高级语言更接近人性化，所以编程效率更高。



动态类型语言和静态类型语言
======================================================================================================================================================
	
    动态类型语言：python、Ruby、JS
        
        动态语言和动态类型语言是不同的两个概念。

        动态语言：是一类在运行时可以改变其结构的语言：例如新的函数、对象、甚至代码可以被引进，
        已有的函数可以被删除或是其他结构上的变化。通俗点说就是在运行时代码可以根据某些条件改变自身结构。
        这里的结构是代码结构，动态类型语言的数据类型不是在编译阶段决定的，而是把类型绑定延后到了运行阶段。
        
        动态类型语言：是指在运行期间才去做数据类型检查的语言，说的是数据类型
    
    静态类型语言：c，c++，java
        
        静态类型语言分为两种：explicitly typed显式类型、implicity typed隐式类型。
            静态显式类型 ：Java/C

            静态隐式类型 ：Ocaml, Haskell
            
        静态语言：与动态语言相对应的，运行时结构不可变的语言就是静态语言。
        
        静态类型语言：静态语言的数据类型是在编译期间（或运行之前）确定的，编写代码的时候要明确确定变量的数据类型。
    
    对于静态类型语言，变量类型都是在编译期即确定的，可以进行比较完备的类型检查，避免运行时的类型错误。对于动态类型语言，变量类型是可以动态改变的，无法在编译期确定，因此编译期的类型检查比较弱，这将导致很多类型错误直到运行期才能发现。动态类型语言特点是灵活，缺点是牺牲了部分性能。



强类型语言和弱类型语言
======================================================================================================================================================

		强类型：c#、Python、Java、.net 、C++
			强类型语言： 强类型语言是一种强制类型定义的语言，一旦某一个变量被定义类型，如果不经过强制转换，则它永远就是该数据类型了，强类型语言
		弱类型：vb 、PHP、javascript
			弱类型语言：弱类型语言是一种弱类型定义的语言，某一个变量被定义类型，该变量可以根据环境变化自动进行转换，不需要经过显性强制转换。
			
		无论是强类型语言还是弱类型语言，判别的根本是是否会隐性的进行语言类型转变。强类型语言在速度上略逊于弱类型语言，但是强类型定义语言带来的严谨性又能避免不必要的错误。
		弱类型的语言是没有明显的类型,他能随着环境的不同,自动变换类型，而强类型则没这样的规定,不同类型间的操作有严格定义,只有相同类型的变量才能操作,虽然系统也有一定的默认转换,当绝没有弱类型那么随便。和动态、静态的特点一样，优缺点是灵活和性能之间的抉择。


	
编译型语言，解释型语言
======================================================================================================================================================

    编译型：c，c++
        编译型语言：程序在执行之前需要一个专门的编译过程，把程序编译成 为机器语言的文件，运行时不需要重新翻译，直接使用编译的结果就行了。程序执行效率高，依赖编译器，跨平台性差些。
        运行编译型语言是相对于解释型语言存在的，编译型语言的首先将源代码编译生成机器语言，再由机器运行机器码（二进制）
    解释型：python，JavaScript，Perl，shell
        解释型语言：程序不需要编译，程序在运行时才翻译成机器语言，每执 行一次都要翻译一次。因此效率比较低。相对于编译型语言存在的，源代码不是直接翻译成机器语言，而是先翻译成中间代码，再由解释器对中间代码进行解释运行。
    
    编译型是运行前先由编译器将高级语言代码编译为对应机器的cpu汇编指令集，再由汇编器汇编为目标机器码，生成可执行文件，然最后运行生成的可执行文件，一般生成的可执行文件及.exe文件。
    解释型是在运行时由翻译器将高级语言代码翻译成易于执行的中间代码，并由解释器逐一将该中间代码解释成机器码并执行。
    对于源程序，编译型语言在执行程序中会将源文件一次性的转化为机器码，而解释型语言是边编译边解释。编译型语言是离不开解释程序的，
    这也导致了解释性语言对于运行时候的速度比价慢，解释型语言只要有解释器，移植起来比较方便，而编译型语言则要对于不同的系统进行编译，是的工作繁琐，且在调试程序的时候比较慢。



Python和Java编译过程比较
------------------------------------------------------------------------------------------------------------------------------------------------------

Pyton和Java的执行过程如下图所示：

    .. image:: /Program/res/images/language/others/compare-python-java.jpg
        :width: 400px
        :align: center



面向对象型和面向过程型
======================================================================================================================================================

    面向对象语言：c#、java、Python
        面向对象语言：面向对象语言（Object-Oriented Language）是一类以对象作为基本程序结构单位的程序设计语言，指用于描述的设计是以对象为核心，而对象是程序运行时刻的基本成分。语言中提供了类、继承等成分，有识认性、多态性、类别性和继承性四个主要特点。
        
        面向对象的三个基本特点：封装、继承、多态。
    面向过程语言：c
        面向过程语言：面向过程的语言也称为结构化程序设计语言，是高级语言的一种。
        在面向过程程序设计中，问题被看作一系列需要完成的任务，函数则用于完成这些任务，
        解决问题的焦点集中于函数。其概念最早由E．W．Dijikstra在1965年提出，是软件发展的一个重要里程碑。它的主要观点是采用自顶向下、逐步求精的程序设计方法，
        使用三种基本控制结构构造程序，即任何程序都可由顺序、选择、循环三种基本控制结构构造。

面向过程是决定该怎么铺成一条路到达终点，而面向对象是要用那些具有特定功能的像来做，两者是不同的思想。
面向过程的优点是性能比面向对象高，因为类调用时需要实例化，开销比较大，比较消耗资源，
但像单片机、嵌入式开发、Linux/Unix等一般采用面向过程开发，性能是最重要的因素。缺点是没有面向对象易维护、易复用、易扩展。
而面向对象的优点是易维护、易复用、易扩展，由于面向对象有封装、继承、多态性的特性，可以设计出低耦合的系统，使系统更加灵活、更加易于维护，缺点是性能比面向过程低。




