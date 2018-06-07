## 项目简介
基于soa的架构   
SOA：Service Oriented Architecture面向服务的架构。也就是把工程拆分成服务层、表现层两个工程。服务层中包含业务逻辑，只需要对外提供服务即可。表现层只需要处理和页面的交互，业务逻辑都是调用服务层的服务来实现。
## 系统架构
![](https://github.com/YuuiChung/Taotao/blob/master/images/3.png)
## 项目搭建
### 开发环境分析
开发环境： MyEclipse + Tomcat7 + MySQL + SVN 
软件架构： springMVC + Mybatis + Maven + CentOS+ Solr + Redis + Nginx
### 后台工程搭建分析
Maven的常见打包方式：jar、war、pom
Pom工程一般都是父工程，管理jar包的版本、maven插件的版本、统一的依赖管理。聚合工程。

Taotao-parent：父工程，打包方式pom，管理jar包的版本号。   
　　|　　　　　　项目中所有工程都应该继承父工程。   
|--Taotao-common：通用的工具类通用的pojo。打包方式jar   
|--Taotao-manager：服务层工程。聚合工程。Pom工程   
　　|--taotao-manager-dao：打包方式jar   
　　|--taotao-manager-pojo：打包方式jar   
　　|--taotao-manager-interface：打包方式jar   
　　|--taotao-manager-service：打包方式：war   
|--taotao-manager-web：表现层工程。打包方式war   
### 启动工程
启动tomcat插件：
clean tomcat7:run
先把taotao-parent、taotao-common安装到本地仓库。然后再启动。
配置服务层工程、表现层工程启动
![](https://github.com/YuuiChung/Taotao/blob/master/images/1.png)
![](https://github.com/YuuiChung/Taotao/blob/master/images/2.png)

## 感谢
黑马程序员[http://www.itheima.com/](http://www.itheima.com/)


