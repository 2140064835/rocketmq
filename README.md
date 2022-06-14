## Apache RocketMQ 
[![Build Status](https://travis-ci.org/apache/rocketmq.svg?branch=master)](https://travis-ci.org/apache/rocketmq) [![Coverage Status](https://coveralls.io/repos/github/apache/rocketmq/badge.svg?branch=master)](https://coveralls.io/github/apache/rocketmq?branch=master)
[![CodeCov](https://codecov.io/gh/apache/rocketmq/branch/master/graph/badge.svg)](https://codecov.io/gh/apache/rocketmq)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.apache.rocketmq/rocketmq-all/badge.svg)](http://search.maven.org/#search%7Cga%7C1%7Corg.apache.rocketmq)
[![GitHub release](https://img.shields.io/badge/release-download-orange.svg)](https://rocketmq.apache.org/dowloading/releases)
[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)
[![Average time to resolve an issue](http://isitmaintained.com/badge/resolution/apache/rocketmq.svg)](http://isitmaintained.com/project/apache/rocketmq "Average time to resolve an issue")
[![Percentage of issues still open](http://isitmaintained.com/badge/open/apache/rocketmq.svg)](http://isitmaintained.com/project/apache/rocketmq "Percentage of issues still open")
[![Twitter Follow](https://img.shields.io/twitter/follow/ApacheRocketMQ?style=social)](https://twitter.com/intent/follow?screen_name=ApacheRocketMQ)

**[Apache RocketMQ](https://rocketmq.apache.org) is a distributed messaging and streaming platform with low latency, high performance and reliability, trillion-level capacity and flexible scalability.**

It offers a variety of features:

* Messaging patterns including publish/subscribe, request/reply and streaming
* Financial grade transactional message
* Built-in fault tolerance and high availability configuration options base on [DLedger](https://github.com/openmessaging/openmessaging-storage-dledger)
* A variety of cross language clients, such as Java, [C/C++](https://github.com/apache/rocketmq-client-cpp), [Python](https://github.com/apache/rocketmq-client-python), [Go](https://github.com/apache/rocketmq-client-go), [Node.js](https://github.com/apache/rocketmq-client-nodejs)
* Pluggable transport protocols, such as TCP, SSL, AIO
* Built-in message tracing capability, also support opentracing
* Versatile big-data and streaming ecosystem integration
* Message retroactivity by time or offset
* Reliable FIFO and strict ordered messaging in the same queue
* Efficient pull and push consumption model
* Million-level message accumulation capacity in a single queue
* Multiple messaging protocols like JMS and OpenMessaging
* Flexible distributed scale-out deployment architecture
* Lightning-fast batch message exchange system
* Various message filter mechanics such as SQL and Tag
* Docker images for isolated testing and cloud isolated clusters
* Feature-rich administrative dashboard for configuration, metrics and monitoring
* Authentication and authorization
* Free open source connectors, for both sources and sinks
* Lightweight real-time computing
----------

## Apache RocketMQ Community
* [RocketMQ Streams](https://github.com/apache/rocketmq-streams)
* [RocketMQ Flink](https://github.com/apache/rocketmq-flink)
* [RocketMQ Client CPP](https://github.com/apache/rocketmq-client-cpp)
* [RocketMQ Client Go](https://github.com/apache/rocketmq-client-go)
* [RocketMQ Client Python](https://github.com/apache/rocketmq-client-python)
* [RocketMQ Client Nodejs](https://github.com/apache/rocketmq-client-nodejs)
* [RocketMQ Spring](https://github.com/apache/rocketmq-spring)
* [RocketMQ Exporter](https://github.com/apache/rocketmq-exporter)
* [RocketMQ Operator](https://github.com/apache/rocketmq-operator)
* [RocketMQ Docker](https://github.com/apache/rocketmq-docker)
* [RocketMQ Incubating Community Projects](https://github.com/apache/rocketmq-externals)

----------
## Learn it & Contact us
* Mailing Lists: <https://rocketmq.apache.org/about/contact/>
* Home: <https://rocketmq.apache.org>
* Docs: <https://rocketmq.apache.org/docs/quick-start/>
* Issues: <https://github.com/apache/rocketmq/issues>
* Rips: <https://github.com/apache/rocketmq/wiki/RocketMQ-Improvement-Proposal>
* Ask: <https://stackoverflow.com/questions/tagged/rocketmq>
* Slack: <https://rocketmq-invite-automation.herokuapp.com/>
 

----------



## Contributing
We always welcome new contributions, whether for trivial cleanups, [big new features](https://github.com/apache/rocketmq/wiki/RocketMQ-Improvement-Proposal) or other material rewards, more details see [here](http://rocketmq.apache.org/docs/how-to-contribute/).
 
----------
## License
[Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html) Copyright (C) Apache Software Foundation


----------
## Export Control Notice
This distribution includes cryptographic software. The country in which you currently reside may have
restrictions on the import, possession, use, and/or re-export to another country, of encryption software.
BEFORE using any encryption software, please check your country's laws, regulations and policies concerning
the import, possession, or use, and re-export of encryption software, to see if this is permitted. See
<http://www.wassenaar.org/> for more information.

The U.S. Government Department of Commerce, Bureau of Industry and Security (BIS), has classified this
software as Export Commodity Control Number (ECCN) 5D002.C.1, which includes information security software
using or performing cryptographic functions with asymmetric algorithms. The form and manner of this Apache
Software Foundation distribution makes it eligible for export under the License Exception ENC Technology
Software Unrestricted (TSU) exception (see the BIS Export Administration Regulations, Section 740.13) for
both object code and source code.

The following provides more details on the included cryptographic software:

This software uses Apache Commons Crypto (https://commons.apache.org/proper/commons-crypto/) to
support authentication, and encryption and decryption of data sent across the network between
services.

RocketMQ核心目录说明如下:
1)broker: broker模块(broker启动进程)
2)client: 消息客户端,包含消息生产者,消息消费者相关类
3)common: 公共包
4)dev: 开发者信息(非源代码)
5)distribution: 部署实例文件(非源代码)
6)example: RocketMQ示例代码
7)filter: 消息过滤相关基础类
8)namesrv: NameServer实现相关类(NameServer启动进程)
9)openmessaging: 消息开放标准
10)remoting: 远程通信模块,基于netty
11)srvutil: 服务器工具类
12)store: 消息存储实现相关类
13)style: checkstyle相关实现
14)tools: 工具类,监控命令相关实现类

1.3 RocketMQ 的设计理念和目标
1.3.1 设计理念
       RocketMQ 设计基于主题的发布与订阅 模式 其核心功能包括消息发送、 消息存储 Broker）、消息消费、路由发现:
       1)是自研 NameServer来实现元数据的管理(Topic 路由信息等)因为 Topic 路由信息无须在集群之间保持强一致，追求最终一致性，并且能容忍分钟级的不一致,
         正是基于此种情况 RocketMQ NameServer 集群之间互不通信，极大地降低了 NameSe ve 现的 复杂程度， 对网络的要求也降低了不少;
       2)是高效的 IO 存储机 RocketMQ 求消息发送的高吞吐量,RocketMQ 消息存储文件设计成文件组的概念，组内单个文件大小固定，方便引人内存 映射机制，所有主
         题的消息存储基于顺序写 极大地提供了消息写性能， 同时为了兼顾消息消费与消息查找，引入了消息消费队列文件与索引文件
       3)只保证消息被消费者消费，但设计上允许消息被重复消费，这样极大 化了消息中间件的内核，使得实现消息发送高可用变得非常简单与高效消息重复问题由消费者
         在消息消费时实现幕等
1.3.2 设计目标
      1. 架构模式
      RocketMQ 与大部分消息中间件一样，采用发布订阅模式，基本的参与组件主要包括消息发送者、消息服务器（消息存储）、消息消费、路由发现
      2. 顺序消患
      所谓顺序消息，就是消息消费者按照消息达到消息存储服务器的顺序消费 rocketMQ可以严格保证消息有序
      3. 消息过滤
      消息过滤是指在消息消费时，消息消费者可以对同一主题下的消息按照规定只消费自己感兴趣的消息 RocketMQ 消息过滤支持在服务端与消费端的消息过滤机制
      1）消息在Broker端过滤,Broker只将消息消费者感兴趣的消息发送给消息消费者
      2）消息在消息消费端过滤,消息过滤方式完全由消息消费者自定义，但缺点是有很多,无用的消息会从 Broker传输到消费端
      4. 消息存储
      消息中间件的一个核心实现是消息的存储 对消息存储一般有如下两个维度的考量,消息堆积能力和消息存储性能,RocketMQ 追求消息存储的高性能,引人内存映射机制，
      所有主题的消息顺序存储在同一个文件中,同时为了避免消息无限在消息存储服务器中累积，引入了消息文件过期机制与文件存储空间报警机制
      5. 消息高可用性
      通常影响消息可靠性的有以下几种情况
      1) Broker 正常关机
      2) Broker 异常 Crash
      3) OS Crash
      4）机器断电，但 能立即恢复供电情况
      5）机器无法开机（可能是 CPU 、主板、 内存等关键设备损坏）
      6）磁盘设备损坏
      针对上述情况，情况 1~4 RocketMQ 在同步刷盘机制下可以确保不丢失消息，在异步刷盘模式下，会丢失少量消息 情况 5-6 属于单点故障，一旦发生，
      该节点上的消息全部丢失，如果开启了异步复制机制，RoketMQ 能保证只丢失少量消息，RocketMQ 在后续版本中将引人双写机制，以满足消息可靠性要求极高的场合
      6. 消息到达(消费)低延迟
      RocketMQ 在消息不发生消息堆积时，以长轮询模式实现准实时的消息推送模式
      7. 确保消息必须被消费一次
      RocketMQ 通过消息消费确认机制（ACK）来确保消息至少被消费一次 ，但由于ACK消息有可能丢失等其他原因，RocketMQ 无法做到消息只被消费一次,有重复消费的可能
      8. 回溯消息
      回溯消息是指消息消费端已经消费成功的消息，由于业务要求需要重新消费消息,RocketMQ 支持按时间回溯消息，时间维度可精确到毫秒，可以向前或向后回溯
      9.消息堆积
      消息中间件的主要功能是异步解锢，必须具备应对前端的数据洪峰，提高后端系统的可用性，必然要求消息中间件具备一定的消息堆积能力,RocketMQ 消息存储使用磁盘文件
      （内存映射机制），并且在物理布局上为多个大小相等的文件组成逻辑文件组，可以无限循环
      使用 RocketMQ 消息存储文件并不是永久存储在消息服务器端，而是提供了过期机制，默
      认保留
      10. 定时消息
      时消息是指消息发送到 Broker 后， 不能被消息消费端立即消费，要到特定的时间点
      或者等待特定的时间后才能被消费 如果要支持任意精度的定时消息消费，必须在消息服
      务端对消息进行排序，势必带来很大的性能损耗，故 RocketMQ 不支持任意进度的定时消
      息，而只支持特定延迟级别
      11 消息重试机制
      消息重试是指消息在消费时，如果发送异常，消息中间件需要支持消息重新投递，
      RocketMQ 支持消息重试机