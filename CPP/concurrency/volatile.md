1. volatile 阻止编译器优化内存的读写
   ```c++
   volatile int x;
   auto y = x;     // read x
   y = x;          // read x again (can't be optimized away)

   x = 10;         // write x ( can't be optimized away)
   x = 20;         // write again

*参考：<<Effective Modern C++>> 的 (Item 40)*
