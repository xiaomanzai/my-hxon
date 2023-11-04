
## 通过@ComponentScan 来配置


扫描需要交给ioc容器的包

ps：会覆盖springboot自己默认的扫描包，需要重庆配置springboot的包


## 通过@Import注解

1. 可以import 按照类名
2. 可以导入一个配置类，配置类里所有的bean都会交给ioc容器管理
3. 可以导入一个importselector 的实现类 使用selectimports，返回一个string的数组
4. 可以import包自定义的接口


## spring boot自动配置
实际上是通过@import 配置了一些依赖

通过注解@Autocofig 的直接 调用 @import 来导入一个文件来，此文件夹包括所有的全类名

## @conditional

使用：在配置@Bean的后面来进行定义

@ConditionalOnClass 判断环境中是否有对应字节码文件，才注册bean到ioc容器中

@ConditionalOnMissingBean 判断环境中有没有对应的bean

@ConditionalOnProperty 判断配置文件中有对应属性和值，才注册bean'到IOC容器中


