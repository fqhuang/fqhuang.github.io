# Flink流计算编程--Pravega+Flink

——分布式流存储Pravega系列7

> 作者：滕昱、黄飞情

## 1、简介

### 1.1 Pravega flink connector

Pravega flink connector库提供了一个数据源（source）和数据接收器（sink），可与Flink Streaming API一起使用，也可将Pravega stream用作Flink批处理程序中的数据源，

### 功能 & 亮点

- 为读写客户端提**仅一次处理（Exactly-once）**保证, 支持端到端的**仅一次处理**。
- 与 flink 的checkpoints和savepoints无缝集成。
- 支持读写客户端高吞吐量和低延迟处理的并行。
- 对Pravega streams的batch和streaming访问用例提供Table API。




## 6、总结

Pravega作为一个实时流存储，本身具有高吞吐、低延时、持久化、分布式等特点，其仅一次处理 (exactly-once)和实时动态的弹性扩展，使得可靠性和性能都可以很好的保证。Pravega+Flink的架构，可以使flink只需关注计算本身。

有关Pravega的更多详细信息，请参阅官方网站以及关注我们的后续文章。

## Pravega系列文章计划
Pravega根据Apache 2.0许可证开源，我们欢迎对流式存储感兴趣的大咖们加入Pravega社区，与Pravega共同成长。下一篇文章将会从Pravega的应用实例出发，阐述如何使用Pravega。本篇文章为Pravega系列第二篇，后面的文章标题如下（标题根据需求可能会有更新）：

1. 实时流处理(Streaming)统一批处理(Batch)的最后一块拼图:Pravega
2. **Pravega设计原理与基本架构介绍**
3. Pravega应用实例
4. Pravega动态弹性伸缩特性
5. Pravega的仅一次语义及事务支持
6. 分布式一致性解决方案：状态同步器
7. 与Apache Flink集成使用


## 作者简介

- 滕昱：就职于 DellEMC 非结构化数据存储部门 (Unstructured Data Storage) 团队并担任软件开发总监。2007 年加入 DellEMC 以后一直专注于分布式存储领域。参加并领导了中国研发团队参与两代 DellEMC 对象存储产品的研发工作并取得商业上成功。从 2017 年开始，兼任 Streaming 存储和实时计算系统的设计开发与领导工作。
- 黄飞情，现就职于DellEMC，10年+ 存储、分布式虚拟化、云计算开发以及架构设计经验，现从事流存储和实时计算系统的设计与开发工作；
- 周煜敏，复旦大学计算机专业研究生，从本科起就参与 DellEMC 分布式对象存储的实习工作。现参与 Flink 相关领域研发工作。


## 参考链接

1. https://www.pravega.io
2. <http://pravega.io/connectors/flink/docs/latest/>
