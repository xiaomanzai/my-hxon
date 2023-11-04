
## 获取 


从ioc容器当中获取bean容器

applicationContext 的方法 getbean（）

1. 通过 Object getbean(string s)来获取
2. 通过 \<T> getbean(\<T> clssname) 来获取
3. 通过\<T> getbean(string s,\<T > classname) 来获取

spring项目启动的时候会把bean创建好在ioc容器当中
## 作用域

- singleton 容器内的bean只会有一个实例(默认,并在ioc容器第一次初始化的时候一起实例化  )
- prototype 每次使用该bean 时会创建新的实例(非单列)
- request 请求范围内创建实例
- session 会话范围内创建实例
- application 每个应用范围内会创建新的实例
## 第三方bean管理

定义一个cofig类来 通过注解@Bean来定义第三方bean交给ioc容器管理

此时在进行依赖注入的时候，实现类的名称为@Bean注解的方法名


