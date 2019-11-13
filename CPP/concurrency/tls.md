### Thread-Local Storage

#### _thread key-word

1. _____thread 是 GCC 内置的线程局部存储,性能可与全局变量媲美

1. __thread 可以单独使用，或者只能跟在 extern / static 后面
    ```c++
    __thread int i;
    extern __thread int i;
    static __thread int i;

1. __thread 可以修饰全局变量、静态变量，不能修饰函数的局部变量和 class 普通成员变量

1. __thread 只能使用编译期常量初始化 __thread 变量


#### thread_local key-word

1. 从 c++11 开始，可以使用 thread_local 定义线程局部变量，没有 __thread 的其他限制
