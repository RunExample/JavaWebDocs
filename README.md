# JavaWebDocs
documents for java web

## 概念

为了简化描述，为了解释各个概念之间的关系，如下给出各个概率不严格的定义

### NIO

Java Non-blocking IO库，感觉像socket + select/poll/epoll，可以说是Java的IO底层库

例子参见<https://github.com/RunExample/JavaWebBasic/tree/master/NIO>

### Servlet以及Tomcat

参见 <https://www.javatpoint.com/servlet-tutorial>

Servlet粗略理解为Java特有的Web请求动态资源的Handler

Tomcat可看做能够处理Servlet请求的Web Server(Servlet Container)
处理静态文件资源相当于一个文件服务器，处理动态API请求则作为Servlet Container，
运行Servlet，需要配置路由规则。

参见 <https://github.com/RunExample/Tomcat>
