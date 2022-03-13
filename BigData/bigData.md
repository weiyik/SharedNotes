# Learning Path

1. Programming Languages
   - Java
   - Scala
   - Python
   - Go
2. Linux
3. Database - SQL
4. Computer Systems
   - Network
   - OS
   - Data Structure and Algorithm
   - Computer Organization
5. [Java Fundamental](Java.md)
   - Lock
   - Multi-threading
   - JUC
   - JVM
   - NIO
   - RPC
6. Distributes Systems
   - Consistency, 2PC, 3PC
   - CAP
   - Time, Clock, event order
   - Paxos
   - Raft, Zab
   - Leader-election, Quorums, lease
   - Distributed Locks
   - Distributed Transaction
   - Distributed ID Generator
7. Network
   - Protocols
   - I/O model: BIO/AIO/NIO
   - Netty
     - Netty 三层网络架构：Reactor通信调度层、职责链PipeLine、业务逻辑处理层
     - Netty 的线程调度模型
     - Netty的核心组件:
       - Channel
       - EventLoop
       - ChannelFuture
       - EventLoopGroup
       - ChannelHandler
       - ChannelPipeLine
       - ChannelHandlerContext
     - ByteBuf
     - TCP/IP粘包拆包
     - 编/解码器
     - 零拷贝、内存池设计
8. Offline Computation
   - MapReduce
   - HDFS
   - YARN
   - Hive
   - Hbase
9. Message Queue
   - [Kafka](Kafka.md)
   - [Pulsar](Pulsar.md)
10. Real-time Computation
    - Flink
      - Ali Course: https://developer.aliyun.com/learning/course/58
      - https://flink-learning.org.cn/
    - [Spark](Spark.md)
11. Data Scheduling/Governance
    - Dolphin Scheduler
    - Data Governance
    - 数据血缘存储和分析
12. Data Warehouse, Data Lake
    - Data warehouse theories: normal form, layering model
    - Common issue: data goverance, metadata mgmt.
    - Data lake: Hudi, IceBerg
13. OLAP
    - Hive, Hawq, Impala: based on SQL on Hadoop
    - Presto: parse sql and generate execution plan
    - Kylin: pre-computing, trade space for time
    - Druid: data realtime-ingestion and realtime-computing
    - ClickHouse: like Hbase in OLAP world, performant in single-table query
    - Greenpulm: like PostgreSQL in OLAP world
14. Algorithm
    - Common algos: reverse order, topN, Bloom filter, dictionary tree
    - Common machine learning algos
    - Algorithm engineering
15. Back-end
    - Spring
    - MyBatis
    - Springboot
16. Business
    - 技术选型
    - 成本控制
    - ROI 投资回报率



Reference:  

1. [群主王知无 大数据技术与架构](https://mp.weixin.qq.com/s/cBncBEJ5e_NtwiOa1VWFfQ)