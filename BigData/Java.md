# Java

- [Java](#java)
  - [Java语言基础](#java语言基础)
  - [锁](#锁)
  - [多线程](#多线程)
  - [并发](#并发)
  - [JVM](#jvm)
  - [NIO](#nio)
  - [RPC](#rpc)

## Java语言基础

- Java 的面向对象
- Java 语言的三大特征：封装、继承和多态
- Java 语言数据类型
- Java 的自动类型转换，强制类型转换
- Java 语言中的关键字：final、static、transient、instanceof、volatile、synchronized的底层原理
  - transient：修饰字段，不会被序列化
- Java 中常用的集合类的实现原理：ArrayList/LinkedList/Vector、SynchronizedList/Vector、HashMap/HashTable/ConcurrentHashMap互相的区别以及底层实现原理
  - Vector: array-like, synchronized
  - Collections.synchronizedList/synchronizedCollection/synchronizedSet ..., returns a synchronized (thread-safe) collection backed by the specified collection.
    ```java
      Collection c = Collections.synchronizedCollection(myCollection);
        ...
      synchronized (c) {
          Iterator i = c.iterator(); // Must be in the synchronized block
          while (i.hasNext())
            foo(i.next());
      }
    ```
- 枚举
- IO
- 反射
- 注解
- Lambda表达式
- 动态代理

## 锁

- CAS、乐观锁与悲观锁、数据库相关锁机制、分布式锁、偏向锁、轻量级锁、重量级锁、monitor
- 锁优化、锁消除、锁粗化、自旋锁、可重入锁、阻塞锁、死锁
- 死锁的原因和解决办法
- CountDownLatch、CyclicBarrier 和 Semaphore 三个类的使用和原理

## 多线程

- 并发和并行的区别
- 线程与进程的区别
- 线程的实现、线程的状态、优先级、线程调度、创建线程的多种方式、守护线程
- 自己设计线程池、submit() 和 execute()、线程池原理
- 为什么不允许使用 Executors 创建线程池
- 死锁、死锁如何排查、线程安全和内存模型的关系
- ThreadLocal变量
- Executor创建线程池的方式：
- ThreadPoolExecutor创建线程池、拒绝策略
- 线程池关闭的方式

跟线程安全相关：

- 线程安全
- 多级缓存和一致性
- CPU的时间片和原子性
- 指令重排序
- 内存模型
- Happens-before
- as-if-serial

## 并发

- 同步容器与并发容器
  - JUC 包中 List 接口的实现类：CopyOnWriteArrayList
  - JUC 包中 Set 接口的实现类：CopyOnWriteArraySet、ConcurrentSkipListSet
  - JUC 包中 Map 接口的实现类：ConcurrentHashMap、ConcurrentSkipListMap
  - JUC包中Queue接口的实现类：ConcurrentLinkedQueue、ConcurrentLinkedDeque、ArrayBlockingQueue、LinkedBlockingQueue、LinkedBlockingDeque
- Thread
- Runnable&Callable
- ReentrantLock
- ReentrantReadWriteLock
- Atomic包
- Semaphore
- CountDownLatch
- ConcurrentHashMap
- Executors

## JVM

[Reading notes of 《深入理解Java虚拟机》](../Java/JVM/0.toc.md)

- JVM内存结构
- 堆和栈
- Java内存模型
- 垃圾回收
  - GC算法：标记清除、引用计数、复制、标记压缩、分代回收、增量式回收
  - GC参数
  - 垃圾收集器（CMS、G1、ZGC、Epsilon）
  - 对象存活的判定
- JVM参数及调优
- JAVA对象模型
- 虚拟机性能监控与故障处理工具
- 即时编译器、编译优化
- 类加载机制
- 虚拟机性能监控与故障处理工具
  - jps
  - jstack
  - jmap
  - jstat
  - jconsole
  - jinfo
  - jhat
  - javap
  - btrace
  - TProfiler
  - jlink
  - Arthas

## NIO

- 用户空间以及内核空间
- Linux 网络 I/O 模型：阻塞 I/O (Blocking I/O)、非阻塞 I/O (Non-Blocking I/O)、I/O 复用（I/O Multiplexing)、信号驱动的 I/O (Signal Driven I/O)、异步 I/O
- 零拷贝（ZeroCopy）
- BIO、AIO、NIO 对比
- 缓冲区 Buffer
- 通道 Channel
- 反应堆 Reactor
- 选择器 Selector
- epoll

## RPC

- RPC 的原理编程模型
- 常用的 RPC 框架：Thrift、Dubbo、SpringCloud
- RPC 的应用场景和与消息队列的差别
- RPC 核心技术点：服务暴露、远程代理对象、通信、序列化
