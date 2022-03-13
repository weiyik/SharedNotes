# Spark

## Spark Core(⭐️⭐️⭐️⭐️⭐️)

- Spark的集群搭建和集群架构（Spark 集群中的角色）
- Spark Cluster 和 Client 模式的区别
- Spark 的弹性分布式数据集 RDD
- Spark DAG（有向无环图）
- 掌握 Spark RDD 编程的算子 API（Transformation 和 Action 算子）
- RDD 的依赖关系，什么是宽依赖和窄依赖
- RDD 的血缘机制
- Spark 核心的运算机制
- Spark 的 CheckPoint 和容错
- Spark 的通信机制
- Spark Shuffle 原理和过程
- Spark Streaming
- 原理剖析（源码级别）和运行机制
- Spark Dstream 及其 API 操作
- Spark Streaming 消费 Kafka 的两种方式
- Spark 消费 Kafka 消息的 Offset 处理
- 数据倾斜的处理方案
- Spark Streaming 的算子调优
- 并行度和广播变量
- Shuffle 调优

## Spark SQL(⭐️⭐️⭐️⭐️⭐️)

- Spark SQL 的原理和运行机制
- Catalyst 的整体架构
- Spark SQL 的 DataFrame
- Spark SQL 的优化策略：内存列式存储和内存缓存表、列存储压缩、逻辑查询优化、Join 的优化
- Catalyst、Tunsten

## Structured Streaming、Spark Streaming(⭐️⭐️⭐️⭐️)
> 这两块部分优先级有所降低，因为Flink社区的蓬勃发展，基于Flink的大数据实时计算技术栈未来会是第一选择。

Spark 从 2.3.0 版本开始支持 Structured Streaming，它是一个建立在 Spark SQL 引擎之上可扩展且容错的流处理引擎，统一了批处理和流处理。正是 Structured Streaming 的加入使得 Spark 在统一流、批处理方面能和 Flink 分庭抗礼。

- Structured Streaming 的模型
- Structured Streaming 的结果输出模式
- 事件时间（Event-time）和延迟数据（Late Data）
- 窗口操作
- 水印
- 容错和数据恢复

## Spark Mlib、GraphX(⭐️⭐️⭐️)

本部分是 Spark 对机器学习支持的部分，我们学有余力的同学可以了解一下 Spark 对常用的分类、回归、聚类、协同过滤、降维以及底层的优化原语等算法和工具。可以尝试自己使用 Spark Mlib 做一些简单的算法应用。