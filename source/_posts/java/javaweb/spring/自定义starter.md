

## [[springboot自动配置的方案]] 

前置知识


## 如何配置


#### 第一步

新建一个模块，名称为 xxx-spring-boot-starter

新建一个模块，名称为 xxx-spring-boot-autoconfigure


#### 第二步

在starter里面仅仅是引入autoconfigure的mave 包

#### 第三步

在autoconfigure里面自定义你要把他作为java的类

定义一个autoconfiguration的类，把你写的类定义成spring bean 交给ioc容器管理

如果有一些properties的类需要用到配置文件
	则需要用@EnableAutoconfiguration来提前把这个类注入到ioc容器中

#### 最后一步

导入到你的项目maven中，仅仅需要导入starter的maven包就行了

## having enjoing coding
