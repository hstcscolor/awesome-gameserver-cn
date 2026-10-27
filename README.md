# 游戏服务器资源大全
***
### 目录
- [游戏服务器资源大全](#游戏服务器资源大全)
    - [网络](#网络)
    - [协议](#协议)
    - [持久化](#持久化)
    - [缓存与消息队列](#缓存与消息队列)
    - [Log](#log)
    - [游戏AI](#游戏ai)
    - [工具库](#工具库)
    - [开源服务器](#开源服务器)
    - [容器与编排](#容器与编排)
    - [运维](#运维)
    - [学习资源](#学习资源)
    - [其他](#其他)

### 网络
*网络相关的库和工具*
* Java
    * [Netty](https://github.com/netty/netty) - Netty是一个高性能、异步事件驱动的NIO框架，它提供了对TCP、UDP和文件传输的支持
    * [Mina](https://github.com/apache/mina) - Apache Mina是一个能够帮助用户开发高性能和高伸缩性网络应用程序的框架
* C++
    * [libevent](http://libevent.org/) - libevent是一个轻量级的基于事件驱动的高性能的开源网络库,并且支持多个平台
    * [libev](http://software.schmorp.de/pkg/libev.html) - 较libevent而言，设计更简练，性能更好，但对Windows支持不够好
    * [libuv](https://github.com/libuv/libuv) - libuv 是 Node 的新跨平台抽象层,用于抽象 Windows 的 IOCP 及 Unix 的 libev
    * [asio](https://github.com/chriskohlhoff/asio) - 跨平台 C++ 网络与底层 I/O 库，Boost.Asio 的独立版本
    * [muduo](https://github.com/chenshuo/muduo) - 陈硕出品的基于 Reactor 模式的现代 C++ 网络库
    * [evpp](https://github.com/Qihoo360/evpp) - 360 出品的现代 C++ 高性能网络库
    * [KCP](https://github.com/skywind3000/kcp) - 快速可靠的 ARQ 协议，比 TCP 浪费带宽换低延迟
    * [enet](https://github.com/lsalzman/enet) - 面向游戏的可靠 UDP 网络库
* Go
    * [gnet](https://github.com/panjf2000/gnet) - 高性能、轻量级、非阻塞的事件驱动 Go 网络框架
    * [netpoll](https://github.com/cloudwego/netpoll) - 字节跳动开源的高性能 Go 网络库
* Python
    * [Twisted](http://twistedmatrix.com/) - Twisted是用Python实现的基于事件驱动的网络引擎框架
    * [Gevent](http://www.gevent.org/) - Gevent是一种基于协程的Python网络库，它用到Greenlet提供的，封装了libevent事件循环的高层同步API
* Erlang
    * [ranch](https://github.com/ninenines/ranch) - cowboy 项目下的Tcp网络库
* C#
    * [DotNetty](https://github.com/Azure/DotNetty) - netty 的C#版
* Rust
    * [tokio](https://github.com/tokio-rs/tokio) - Rust 异步运行时与网络库事实标准
    * [mio](https://github.com/tokio-rs/mio) - Rust 底层非阻塞 IO 库

### 协议
*协议*
* [protobuf](https://github.com/google/protobuf) - 大家都知道的protobuf
* [FlatBuffers](https://github.com/google/flatbuffers) - Google出品，专门为游戏开发或其他性能敏感的应用程序需求而创建
* [Json](http://www.json.org/) - 这个算凑数吗？
* [MessagePack](https://msgpack.org/) - It's like JSON. but fast and small.
* [Cap'n Proto](https://github.com/capnproto/capnproto) - 极致性能的序列化协议，零拷贝
* [Thrift](https://github.com/apache/thrift) - Apache 跨语言 RPC 与序列化框架
* [CBOR](https://cbor.io/) - 二进制对象表示，IETF RFC 8949
* [SBE](https://github.com/real-logic/simple-binary-encoding) - 面向超低延迟场景的二进制编码

### 持久化
*持久化框架*
* Java
    * [MyBatis](https://github.com/mybatis/mybatis-3) - 一个支持普通SQL查询,存储过程和高级映射的优秀持久层框架
    * [druid](https://github.com/alibaba/druid) - 阿里巴巴出品 数据库连接池
    * [Hibernate](https://github.com/hibernate/hibernate-orm) - 老牌 Java ORM 框架
    * [HikariCP](https://github.com/brettwooldridge/HikariCP) - 高性能 JDBC 连接池
* C#
    * [Dapper](https://github.com/StackExchange/Dapper) - 是一款轻量级ORM框架
    * [Entity Framework Core](https://github.com/dotnet/efcore) - 微软官方 .NET ORM
* Erlang
    * [mysql-otp](https://github.com/mysql-otp/mysql-otp) -  MySQL driver for Erlang/OTP
* Golang
    * [go-sql-driver](https://github.com/go-sql-driver/mysql) -  MySQL driver for Golang
    * [gorm](https://github.com/go-gorm/gorm) - Go 最流行的 ORM
    * [xorm](https://gitea.com/xorm/xorm) - 简单强大的 Go ORM
    * [sqlx](https://github.com/jmoiron/sqlx) - database/sql 的扩展
* Python
    * [SQLAlchemy](https://github.com/sqlalchemy/sqlalchemy) - Python SQL 工具包与 ORM

### 缓存与消息队列
*游戏服常用的缓存与消息中间件*
* [Redis](https://github.com/redis/redis) - 高性能内存数据库，游戏服务器最常用的缓存
* [KeyDB](https://github.com/Snapchat/KeyDB) - Redis 的多线程分支
* [Redisson](https://github.com/redisson/redisson) - Redis 的 Java 客户端，提供分布式对象与服务
* [go-redis](https://github.com/redis/go-redis) - Redis 的 Go 客户端
* [NATS](https://github.com/nats-io/nats-server) - 高性能云原生消息系统
* [NSQ](https://github.com/nsqio/nsq) - 实时分布式消息平台
* [RabbitMQ](https://github.com/rabbitmq/rabbitmq-server) - 通用消息中间件

### Log
*Log*
* Java
    * [Log4j](https://github.com/apache/log4j) - Apache log4j
    * [Logback](https://github.com/qos-ch/logback) - log4j 作者写的下一代日志框架
* C#
    * [NLog](https://github.com/NLog/NLog) - 支持多平台的C# log库
    * [Serilog](https://github.com/serilog/serilog) - 结构化日志的 .NET 库
* C++
    * [spdlog](https://github.com/gabime/spdlog) - 极快的 C++ 日志库
    * [glog](https://github.com/google/glog) - Google C++ 日志库
* Erlang
    * [Lager](https://github.com/erlang-lager/lager) - A logging framework for Erlang/OTP
* Golang
    * [logrus](https://github.com/sirupsen/logrus) - Structured, pluggable logging for Go
    * [zap](https://github.com/uber-go/zap) - Blazing fast, structured, leveled logging in Go
    * [zerolog](https://github.com/rs/zerolog) - 零分配 JSON logger
* Python
    * [loguru](https://github.com/Delgan/loguru) - 简单易用的 Python 日志库

### 游戏AI
*游戏AI*
* [gdx-ai](https://github.com/libgdx/gdx-ai) - libgdx下的一个ai系统（非常适合参考学习）
* [recastnavigation](https://github.com/recastnavigation/recastnavigation) - 非常高效的寻路系统，和Unity的寻路算法几乎一样
* [Serpent.AI](https://github.com/SerpentAI/SerpentAI) - 游戏代理框架，适合写外挂
* [behaviac](https://github.com/Tencent/behaviac/) - 腾讯开源的行为树框架
* [BehaviorTree.CPP](https://github.com/BehaviorTree/BehaviorTree.CPP) - 现代 C++ 行为树库，机器人/游戏均可用

### 工具库
*工具库*
* Java
    * [disruptor](https://github.com/LMAX-Exchange/disruptor) - 性能高效的线程间通讯库
    * [guava](https://github.com/google/guava) - Google出品的Java工具库
    * [Hutool](https://github.com/dromara/hutool) - 国产小而全的 Java 工具类库
* C++
    * [folly](https://github.com/facebook/folly) - Facebook 开源的 C++ 基础库
    * [abseil-cpp](https://github.com/abseil/abseil-cpp) - Google 通用 C++ 基础库
* Go
    * [viper](https://github.com/spf13/viper) - Go 配置解决方案
    * [cobra](https://github.com/spf13/cobra) - Go 命令行框架
    * [ants](https://github.com/panjf2000/ants) - 高性能 goroutine 池

### 开源服务器
*各种开源游戏服务器*
* [pomelo](https://github.com/NetEase/pomelo) - 网易出品的Node.js游戏服务器框架
* [skynet](https://github.com/cloudwu/skynet) - 云风大神出品Lua游戏服务器框架
* [Scut](https://github.com/ScutGame/Scut) - support C#/Python/Lua 可惜两年没有更新了
* [NoahGameFrame](https://github.com/ketoo/NoahGameFrame) - 一个支持分布式的C++游戏服务器框架
* [TrinityCore](https://github.com/TrinityCore/TrinityCore) - MMO游戏服务器框架,开源的魔兽服务器
* [ryzomcore](https://github.com/ryzom/ryzomcore) - 分布式的游戏服务器，ryzom 的官方开源
* [kbengine](https://github.com/kbengine/kbengine) - 一款开源的MMOG游戏服务端引擎， 仅Python脚本即可简单高效的完成任何游戏逻辑(支持热更新)
* [mqant](https://github.com/liangdas/mqant) - mqant是一款基于Golang语言的简洁,高效,高性能的分布式游戏服务器框架
* [MaNGOS](https://github.com/mangos/MaNGOS) - 开源的魔兽服务器
* [xingo](https://github.com/viphxin/xingo) - 高性能golang网络库，游戏开发脚手架
* [cuberite](https://github.com/cuberite/cuberite) - 我的世界 的开源服务器
* [leaf](https://github.com/name5566/leaf) - 用Golang写的gameserver
* [RockGO](https://github.com/zllangct/RockGO) - 基于ECS，用Golang写的gameserver
* [NettyGameServer](https://github.com/jwpttcg66/NettyGameServer) - 使用netty4.X实现的手机游戏分布式服务器
* [due](https://github.com/dobyte/due) - 一款基于Go语言开发的轻量级分布式游戏服务器框架
* [moon](https://github.com/sniper00/moon) - 基于Actor模型的轻量级游戏服务器框架(Modern C++, Lua)
* [Nakama](https://github.com/heroiclabs/nakama) - Heroic Labs 出品的开源分布式游戏服务器，Go 编写
* [Colyseus](https://github.com/colyseus/colyseus) - Node.js / TypeScript 多人游戏服务器框架
* [nano](https://github.com/lonng/nano) - 轻量级、易用、高性能的 Go 游戏服务器框架
* [Pitaya](https://github.com/topfreegames/pitaya) - Go 编写的可扩展游戏服务器框架，pomelo 思路延续
* [Cellnet](https://github.com/davyxu/cellnet) - Go 高性能事件驱动游戏服务器框架
* [gonet](https://github.com/xtaci/gonet) - Go 编写的简洁游戏服务器框架
* [Photon Quantum/Server (示例)](https://github.com/exitgames) - 业内常用的实时多人方案，部分组件开源

### 容器与编排
*游戏服上云常用的容器与调度*
* [Agones](https://github.com/googleforgames/agones) - 基于 Kubernetes 的专用游戏服编排平台
* [Open Match](https://github.com/googleforgames/open-match) - Google 与 Unity 联合开源的可扩展匹配框架
* [Docker](https://github.com/docker/docker-ce) - 容器化运行时
* [Kubernetes](https://github.com/kubernetes/kubernetes) - 容器编排事实标准

### 运维
*运维工具*
* [LinuxGSM](https://github.com/GameServerManagers/LinuxGSM) - Linux Game Server Managers
* [fabric](https://github.com/fabric/fabric) - 远程执行命令
* [Ansible](https://github.com/ansible/ansible) - 无代理的自动化运维工具
* [supervisor](https://github.com/Supervisor/supervisor) - 进程守护管理工具
* [Prometheus](https://github.com/prometheus/prometheus) - 云原生监控与告警系统
* [Grafana](https://github.com/grafana/grafana) - 通用可视化与监控仪表盘
* [Elasticsearch](https://github.com/elastic/elasticsearch) - 日志检索与分析

### 学习资源
*学习资源*
* [Game Programming Patterns](http://gameprogrammingpatterns.com/) 游戏编程模式
* [game-programmer](https://github.com/miloyip/game-programmer) A Study Path for Game Programmer
* [entity-systems](http://entity-systems.wikidot.com/) 实体系统
* [data-oriented-design](http://www.dataorienteddesign.com/dodmain/) 面向数据的设计
* [architect-awesome](https://github.com/xingshaocheng/architect-awesome) 后端架构师技术图谱
* [Client-Server Game Architecture](https://www.gabrielgambetta.com/client-server-game-architecture.html) - 客户端-服务器架构经典系列文章
* [Awesome GameDev](https://github.com/Calinou/awesome-gamedev) - 综合 gamedev 资源合集
* [awesome-cpp](https://github.com/fffaraz/awesome-cpp) - C++ 资源合集，含游戏方向
* [RespawnStack](https://respawnstack.com) - AI tools directory for game developers

### 其他
* [games](https://github.com/leereilly/games) github上的一个游戏列表
* [awesome-go](https://github.com/avelino/awesome-go) - Go 资源合集，找网络/服务器组件常用
* [awesome-erlang](https://github.com/drobakowski/awesome-erlang) - Erlang 资源合集
