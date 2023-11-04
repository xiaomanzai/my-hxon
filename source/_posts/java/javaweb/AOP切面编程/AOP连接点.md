
可以被AOP被控制的方法

Joinpoint获取方法执行的相关信息

ProceedJoinPoint 是 JoinPoint 的子类型，不能执行 proceed的操作

### 相关API

String  getTarget.getClass(.getName() 获取类名

String getsignature.getName() 获取方法名

T[]  getArgs() 获得参数

T[] proceed  执行，返回返回值

