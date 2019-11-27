# Web Docs
整理一些Web相关的知识点

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

### 分布式

#### CAP

<https://en.wikipedia.org/wiki/CAP_theorem>

* [Consistency]: Every read receives the most recent write or an error
* [Availability]: Every request receives a (non-error) response, without the guarantee that it contains the most recent write
* [Partition tolerance]: The system continues to operate despite an arbitrary number of messages being dropped (or delayed) by the network between nodes
When a network partition failure happens should we decide to
    - Cancel the operation and thus decrease the availability but ensure consistency
    - Proceed with the operation and thus provide availability but risk inconsistency

[Consistency]: https://en.wikipedia.org/wiki/Consistency_(database_systems)
[Availability]: https://en.wikipedia.org/wiki/Availability
[Partition tolerance]: https://en.wikipedia.org/wiki/Network_partition

##### Consistency

Note that consistency as defined in the CAP theorem is quite different from the consistency guaranteed in [ACID] database transactions

[ACID]: https://en.wikipedia.org/wiki/ACID

#### ZAB

ZooKeeper的共识算法（consensus algorithm），早于Raft

[论文原文](./resources/ZAB.pdf)

#### Raft

[论文原文](./resources/raft.pdf)

[中文论文翻译](https://github.com/maemual/raft-zh_cn/blob/master/raft-zh_cn.md)

<https://raft.github.io>

> ### what is consensus?
> * Once they reach a decision on a value, that decision is final
> * a cluster of 5 servers can continue to operate even if 2 servers fail.
> * If more servers fail, they stop making progress (but will never return an incorrect result).


