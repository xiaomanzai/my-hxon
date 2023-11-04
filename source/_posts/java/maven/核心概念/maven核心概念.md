
## 坐标


坐标必须可以定义一个确定的坐标

三个向量：
1. groupid 公司的 id
2. artifactld 一个项目或者项目中一个模块的 id
3. version 版本号

向量的取值

- groupid 公司的域名的倒序
- artifactld 模块的名称，将来作为 maven 工程。
- version  需要自己设定
	- shapshot 表示快照版本，不稳定版本，开发板
	- release 标识发行正式版本


## 标签

packaging 标签：打包

\<packaging\> jar <\/packaging> 打 java 工程
如果 jar 是 war 则是 web 工程打 war 包。
如果是 pom 则是管理其他的工程


scope 范围标签
包括 compile/test/provided/system/runtime/import
- compile
- test
- provided


## [[ POM]]

## 目录结构

- src 源码
- main 主体程序
- java 源代码目录
- com package 目录
- resources 配制目录
- test 测试目录

#### pom 的配置


去超级 pom.xml 配置全局配置


## [[依赖传递]]

## [[maven继承]]

## [[聚合]]


