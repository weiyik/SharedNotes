# Pulsar

![avatar](https://mmbiz.qpic.cn/mmbiz_png/UdK9ByfMT2MAlNURvqPhc1nl3kcMnqI3Ma8YY318T2qMkz8utzpgx6LQ0SdCibuO7iaXNNvLuPrlPT38Sb2PoIOw/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)
Ref: https://mp.weixin.qq.com/s/cBncBEJ5e_NtwiOa1VWFfQ

## Pulsar的核心概念

Topic
Bookie
Broker
Entry
Ledger
MetaData Storage
Journal
等等

## Pulsar的关键特性

- 跨地域复制（geo-replication），单个实例原生支持多个集群（跨集群复制）
- 极低的发布延迟和端到端延迟
- 可无缝扩展到超过一百万个 topic
- 简单的客户端API，支持Java、Go、Python和C++
- 支持多种topic订阅模式：独占订阅、共享订阅、故障转移订阅、键共享（exclusive, shared, failover, key_shared）
- 通过 Apache BookKeeper 提供的持久化消息存储机制保证消息传递
- 由轻量级的无服务器（serverless ）计算框架 Pulsar Functions 实现流原生的数据处理
- 基于 Pulsar Functions 的无服务器连接器框架 Pulsar IO 使得数据更易移入、移出 Apache Pulsar
- 分层式存储可在数据陈旧时，将数据从热存储卸载到冷/长期存储（如S3、GCS）中

## Pulsar的架构设计

一个Pulsar实例由一个或多个Pulsar集群组成。实例中的集群可以在它们之间复制数据。一个Pulsar cluster由三部分组成：

- 一个或者多个 broker ：负责处理和负载均衡 producer 发出的消息，并将这些消息分派给 consumer；Broker 与 Pulsar 配置存储交互来处理相应的任务，并将消息存储在 BookKeeper 实例中（又称 bookies）；Broker 依赖 ZooKeeper 集群处理特定的任务；
- 一个BookKeeper：包含一个或多个 bookie 的 BookKeeper 集群负责消息的持久化存储；
- 一个ZooKeeper：特定于某个Pulsar集群的ZooKeeper集群处理Pulsar集群之间的协调任务。
