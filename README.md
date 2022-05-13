UReport2 是一款基于架构在 Spring 之上纯 Java 的高性能报表引擎，通过迭代单元格可以实现任意复杂的中国式报表。 在 UReport2 中，提供了全新的基于网页的报表设计器，可以在 Chrome、Firefox、Edge 等各种主流浏览器运行（IE 浏览器除外）。使用 UReport2，打开浏览器即可完成各种复杂报表的设计制作

[https://www.w3cschool.cn/ureport](https://www.w3cschool.cn/ureport)

## 单机使用

- 1. 引入 jar 依赖

```xml

<dependency>
    <groupId>com.pig4cloud.plugin</groupId>
    <artifactId>ureport-spring-boot-starter</artifactId>
    <version>0.0.2</version>
</dependency>
```

- application.properties 配置本地文件报错路径

```properties
ureport.debug=false
ureport.disableFileProvider=false
ureport.fileStoreDir=/Users/lengleng/Downloads
ureport.disableHttpSessionReportCache=true
```

## 集群使用

```xml
<dependency>
  <groupId>com.pig4cloud.plugin</groupId>
  <artifactId>ureport-spring-boot-starter</artifactId>
  <version>0.0.1</version>
</dependency>

<dependency>
  <groupId>com.pig4cloud.plugin</groupId>
  <artifactId>oss-spring-boot-starter</artifactId>
  <version>0.0.2</version>
</dependency>
```

- 仅需配置云存储相关参数

```
oss.access-key=lengleng
oss.secret-key=lengleng
oss.bucket-name=aaa
oss.endpoint=http://minio.pig4cloud.com
```

关于 [oss-spring-boot-starter ](https://github.com/pig-mesh/oss-spring-boot-starter)使用可参考，兼容所有 S3 协议的分布式文件存储系统
