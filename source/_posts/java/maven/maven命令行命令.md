

## 工程建立

<font size =5 color = #dfdd7a >mvn archetype:generate</font>


## 操作

###### 清理操作
 mvn clean 
 效果删除 target 项目

###### 编译操作

mvn compile  主程序编译
mvn test-compile 测试程序编译


###### 测试操作

mvn test

ps：这条程序会重新编译 test 目录的文件

###### 打包操作

mvn package 打包 java 工程打 jar 包 web 工程打 war 包

###### 安装

mvn install


## web 工程建立

mvn archetype: generate 后面加一些参数指定 groupid 和 artifildId

web 工程可以依赖 jar 包

