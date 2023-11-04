
## 继承


继承就是用父工程来管理各个子工程

父工程可以用来总的配置配置属性，来配置总的依赖和依赖版本

子工程在使用父工程中有也必须要定义依赖，只不过此时不用定义版本

特别的如果子工程中的依赖版本和父工程的依赖版本有冲突，则会覆盖父工程中的版本


## 实现


父工程中
``` xml[]
<!--打包方式要改为pom-->
<packaging>pom</packaging>


<modules>
 <module><!--子工程--></module>
<\modules>

<!--子工程中-->
<parent>
	<groupId><!--父工程--></groupId>
	<artifactId><!--父工程--></artifactId>
	<version><!--父工程--></version>
</parent>
```


一般都会自动构件好而不用去手动配置



