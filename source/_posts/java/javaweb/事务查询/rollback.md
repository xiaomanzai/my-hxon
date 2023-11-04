
[[springboot的事务控制]]基础用法
### rollbackfor

- springboot的默认事务控制只能对runtime的exception进行rollback
- 对于自己控制的springboot的rollback是无法进行rollback
- 在@transaction后面加上rollbackfor = exception.class就可以对所有的异常抛出进行回滚

## propagation

- 解决事务被另一个事务调用
- ![image.png](https://s2.loli.net/2023/08/26/ys925NSwVzPTmxa.png)

默认的情况下就是共用一个事务，前面的事务回滚那么这个也要回滚
新事物则会挂起原来的事务从而创建一个新事物
