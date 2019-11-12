1. std::atomic 通过特殊的机器指令，保证提供的操作都是原子操作
    ```c++
    std::atomic<int> ai(0);
    ai = 10;    // atomically
    ++ai;       // atomically
    --ai;       // atomically
    x.load();       // atomically
    x.store();       // atomically

2. 阻止编译器和底层硬件重排序代码
    ```c++
    std::atomic<bool> valAvailable(false);
    auto imptValue = computeImportantValue();
    valAvailable = true;

3. std::atomic 没有复制构造函数、复制赋值、移动构造函数、移动赋值
    ```c++
    std::atomic<int> x;
    auto y = x;    // error!
    // y = x 不能通过硬件实现原子操作，所以不允许


*参考：<<Effective Modern C++>> 的 (Item 40)
