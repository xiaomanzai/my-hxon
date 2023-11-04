

## sprintboot配置文件注入

**@value("${配置文件中的key}")**

我的一些配置

``` yaml
spring:  
  
  datasource:  
    url: jdbc:mysql://localhost:3306/test  
    driver-class-name: com.mysql.cj.jdbc.Driver  
    username: root  
    password: Xiaochunbihahaha12?  
  servlet:  
    multipart:  
      max-file-size: 1MB  
      max-request-size: 10MB  
  
mybatis:  
  configuration:  
    log-impl: org.apache.ibatis.logging.stdout.StdOutImpl  
    map-underscore-to-camel-case: true  
  
tencentcos:  
  bucketname: tailes-1319790422  
  secretid: AKIDiKlX8WiiiWAalneMtGTXkokZBmGdnhNs  
  secretkey: MVgswqa9YUHvV1mPrLhv2QirsneMyVuD
```


## yml 配置

后缀
application.properties
application.yml
application.yaml

yaml对空格相对敏感一些

## 一键注入

1. 交给ioc容器管理
2. 属性名相同
3. 前后缀相同 @configurationProperties（prefix = “”）


