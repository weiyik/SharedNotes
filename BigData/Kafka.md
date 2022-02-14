# Kafka

Kafka 是最初由 Linkedin 公司开发，是一个分布式、支持分区的（partition）、多副本的（replica）的分布式消息系统，它的最大的特性就是可以实时的处理大量数据以满足各种需求场景：比如基于 Hadoop 的批处理系统、低延迟的实时系统、Spark 流式处理引擎，Nginx 日志、访问日志，消息服务等等，用 Scala 语言编写，Linkedin 于 2010 年贡献给了 Apache 基金会并成为顶级开源项目。

Kafka 或者类似 Kafka 各个公司自己造的消息'轮子'已经是大数据领域消息中间件的事实标准。Kafka 不满足单纯的消息中间件，也正朝着平台化的方向演进。

关于 Kafka 我们需要掌握：

- Features and use cases
- Concepts: Leader, Broker, Producer, Consumer, Topic, Group, Offset, Partition, ISR
- Architecture
- Election strategy
- What happens while Kafka read and writes messages
- How Kafka sync data(ISR)
- How Kafka implements the sequentiality of messages in partition
- Consumer and consumer group
- Best practice to consume Kafka messages
- How Kafka ensure message delivery reliability and idempotency
- How Kafka implements transaction of message
- How Kafka manage offset
- Kafka file storage mechanism
- How Kafka support Exactly-once
- Comparing Kafka with other meesaging middleware like RocketMQ, etc.
