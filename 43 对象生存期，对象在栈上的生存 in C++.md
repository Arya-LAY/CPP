# 43 对象生存期，对象在栈上的生存 in C++

在栈中创建的对象，一旦超过作用域，就会被自动销毁释放。

在局部函数中创建变量，并返回一个指向它的指针，是错误的。

这时，有两条路可以走，

第一个是在外部创建变量，传入函数体，然后在函数体内部去为他赋值之类的。

第二个是类作用域。类的析构函数是对象在超过作用域时自动调用的，可以在析构函数中，加入delete语句，在构造函数中，加入new语句。这样就可以让避免堆出现问题。
