
## 切入点表达式 execution

主要格式有

<font size=4 color = #77c99b>  
execution(访问修饰符* 返回值 包名.类名.* 方法名(方法参数) throw 异常)
方法参数写的是全类名
</font>

<font color = red>ps: 带*可以省略</font>

#### \*，..号的作用
1. \* 主要用来代表一个字符，可以用来匹配任意一个独立符号，可以代替包名，类名，方法名，方法的单个参数
2. ..可以匹配多个方法的参数，匹配多层包名，意思是匹配多个连续的符号
3. @Pointcut 中可以用||来连接execution
4. 尽量不要使用..来匹配多层包名，<font style = "background: #ffe34a" color = #1e1e1e>要缩小范围</font>进行匹配


## @annotation 

切入点玩表达式，用于匹配注解的方法

@annotation （包名.注解名）
