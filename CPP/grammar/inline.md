### inline

1. inline 必须与函数定义放在一起

2. 定义在类中的成员函数自动成为内联函数

3. 调用点必须能看到内联函数的定义
   > 放到头文件，则只需 include 即可
     放到源码文件，则需要把内联函数的实现放到调用点所在的文件

4. 函数少于 10 行才将其定义为 inline

5. 谨慎对待析构函数，往往比表面看起来更长

6. 内联包含循环或者 switch 语句的函数常常得不偿失

7. 有些声明为内联的函数也不一定被编译器内联，如虚函数、递归函数
