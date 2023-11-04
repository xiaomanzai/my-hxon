
## 组件

可重复调用的对象

## 优势
1. 降低耦合
2. 提高可复用
3. 方便配置
4. 享受 spring 对象的服务


## 实现和理解
[![流程图](https://z1.ax1x.com/2023/10/20/piiXCyq.png)]( https://imgse.com/i/piiXCyq ) ![image.png](https://s2.loli.net/2023/10/20/2BfKzHyPGuNXqLa.png)
## xml 实现

#### 无参数实现
`<bean id = "bean名" class = "全类名">`

#### 工厂模式

1. 静态工厂
`<bean id ="bean名" class ="工厂全类名 " factory-method=“工厂方法”>`

由于 static 方法是先于对象而存在的，因此可以直接调用方法来实例化

2. 非静态工厂
`<bean id = "bean名" class=“工厂全列名”>`
`<bean id = "bean 名" factory-bean="工厂类名" factory-method = "工厂方法">`

其实就是要先创造工厂对象才能调用方法


#### 有参实现（di 依赖注入）

引用和被引用必须都在 ioc 容器里

如果在含参构造中有对象，则此对象必须在 ioc 容器中

`<bean id="bean" class="全类名">
	`<constructor-arg  name ="参数名" value="值" ref="引用"/>`
`</bean>`

如果有多个值则多个构造函数

如果是 set 方法来初始化构造

\<property name="方法名 (不带 set)" value="值" ref ="引用"/>


#### 创造 ioc 容器 xml

`ApplicationContext  classPathXmlApplicationContext = new  classPathXmlApplicationContext ("文件名")`


#### 获取 bean

ioc 对象的 getbean 方法
context. getbean (“bean 名”, 类的全类名)

如果是类的全类名是某个接口的实现列，也可以改成接口

#### ioc 的周期

周期方法：到了对应的周期就会主动调用的方法。
![image.png](https://s2.loli.net/2023/10/20/xRZf5JMohelbGWK.png)

`<bean id="bean 名" class="全类名" init-method="初始化方法名" destroy-method=“销毁方法名”>`

ps: destroy method 要在 ioc 正常的退出才能调用，如果是没有正常退出是无法执行的

`applicationContext. close ()` 来使得 ioc 正常退出

#### ioc 的作用范围
![image.png](https://s2.loli.net/2023/10/20/mB289NRjXIvxk4Q.png)

是通过 beanDefinition 来通过反射来创建对象，一般都是单列
![image.png](https://s2.loli.net/2023/10/20/DIFjkqOwtSsdLMH.png)

#### factoryBean

![image.png](https://s2.loli.net/2023/10/20/fDqedJYGHcEgKZa.png)

方法
![image.png](https://s2.loli.net/2023/10/20/MKPuaiJAUp95c3O.png)

其实就是把工厂放到 ioc 容器中，从而可以自己快速实现自己的实例化方法

工厂 bean 放到 ioc 容器，因此 getbean 可以直接通过工厂的 bean 名，产品类的全类名来直接获得对象

工厂也实例化了，因为工厂不说 static 的方法，工厂的 bean 名是 （&）bean 名

## 注解实现

#### 基础
`@Autowired` 可以 di
相当于 xml 的 set 依赖注入
当定于 `required=false` 的时候则可以表明并不要一定在 ioc 容器中存在这个实现类
如果有多个实现类，可以使用 `@qualifier (value="实现类名")` 来指定实现类

`@Resource (name="类名")` 相当于前面两个注解的组合
这是个 java 提供的注解，但是是由 spring 实现
使用这个注解还需要去导入这个包

`@value` 主要是读外部文件

对于第三方类如 jdbctemplate 需要 xml 第三方注入

#### @bean 注解

bean 注解是在配置类的使用的，可以把配置类的生成方法放置到 ioc 容器中

1. name 定义 ioc 的 bean 名
2. init 方法和 detroy 方法
3. @scope 定义是否单列
4. 如果有其他的类要依赖注入，此时被注入的类要是在 ioc 容器中或者成为形参注入
5. 如果有多个在进行形参注入的时候要等于对应的 beanid

#### @import

可以把一个配置类导入一个配置类中进行集成