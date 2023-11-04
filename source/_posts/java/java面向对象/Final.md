#### final

- 被final修饰的方法不能被重写，类不能被继承

#### 修饰的变量

![](C:\Users\seasyec\AppData\Roaming\marktext\images\2023-03-12-16-49-43-image.png)

- 也就是用了final后尽量不要用改变值和变量名。

- 引用数据类型为什么不能改名字？因为引用数据类型指向的是地址值而不是像基础类型指向的是值。（String被final修饰后就不能被改变名字指向另一个名字，内容因为是private也是不变的）


