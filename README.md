# 游戏服务器资源大全
***
### 目录
- [游戏服务器资源大全](#游戏服务器资源大全)
    - [网络](#网络)
    - [协议](#协议)
    - [持久化](#持久化)
    - [Log](#Log)
    - [游戏AI](#游戏AI)
    - [工具库](#工具库)
    - [开源服务器](#开源服务器)
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
* Python
    * [Twisted](http://twistedmatrix.com/) - Twisted是用Python实现的基于事件驱动的网络引擎框架
    * [Gevent](http://www.gevent.org/) - Gevent是一种基于协程的Python网络库，它用到Greenlet提供的，封装了libevent事件循环的高层同步API
* Erlang
    * [ranch](https://github.com/ninenines/ranch) - cowboy 项目下的Tcp网络库
* C#
    * [DotNetty](https://github.com/Azure/DotNetty) - netty 的C#版

### 协议
*协议*
* [protobuf](https://github.com/google/protobuf) - 大家都知道的protobuf
* [FlatBuffers](https://github.com/google/flatbuffers) - Google出品，专门为游戏开发或其他性能敏感的应用程序需求而创建
* [Json](http://www.json.org/) - 这个算凑数吗？
* [MessagePack](https://msgpack.org/) - It's like JSON. but fast and small.

### 持久化
*持久化框架*
* Java
    * [MyBatis](https://github.com/mybatis/mybatis-3) - 一个支持普通SQL查询,存储过程和高级映射的优秀持久层框架
    * [druid](https://github.com/alibaba/druid) - 阿里巴巴出品 数据库连接池 
* C#
    * [Dapper](https://github.com/StackExchange/Dapper) - 是一款轻量级ORM框架
* Erlang
    * [mysql-otp](https://github.com/mysql-otp/mysql-otp) -  MySQL driver for Erlang/OTP
* Golang 
    * [go-sql-driver](https://github.com/go-sql-driver/mysql) -  MySQL driver for Golang

### Log
*Log*
* Java
    * [Log4j](https://github.com/apache/log4j) - Apache log4j
* C#
    * [NLog](https://github.com/NLog/NLog) - 支持多平台的C# log库
* Erlang 
    * [Lager](https://github.com/erlang-lager/lager) - A logging framework for Erlang/OTP
* Golang
    * [logrus](https://github.com/sirupsen/logrus) - Structured, pluggable logging for Go
    * [zap](https://github.com/uber-go/zap) - Blazing fast, structured, leveled logging in Go


### 游戏AI 
*游戏AI*
* [gdx-ai](https://github.com/libgdx/gdx-ai) - libgdx下的一个ai系统（非常适合参考学习） 
* [recastnavigation](https://github.com/recastnavigation/recastnavigation) - 非常高效的寻路系统，和Unity的寻路算法几乎一样
* [Serpent.AI](https://github.com/SerpentAI/SerpentAI) - 游戏代理框架，适合写外挂
* [behaviac](https://github.com/Tencent/behaviac/) - 腾讯开源的行为树框架

### 工具库
*工具库*
* Java
    * [disruptor](https://github.com/LMAX-Exchange/disruptor) - 性能高效的线程间通讯库
    * [guava](https://github.com/google/guava) - Google出品的Java工具库 
    
 
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

### 运维
*运维工具*
* [LinuxGSM](https://github.com/GameServerManagers/LinuxGSM) - Linux Game Server Managers 
* [fabric](https://github.com/fabric/fabric) - 远程执行命令 

### 学习资源
*学习资源*
* [Game Programming Patterns](http://gameprogrammingpatterns.com/) 游戏编程模式
* [game-programmer](https://github.com/miloyip/game-programmer) A Study Path for Game Programmer
* [entity-systems](http://entity-systems.wikidot.com/) 实体系统
* [data-oriented-design](http://www.dataorienteddesign.com/dodmain/) 面向数据的设计
* [architect-awesome](https://github.com/xingshaocheng/architect-awesome) 后端架构师技术图谱

### 其他
* [games](https://github.com/leereilly/games) github上的一个游戏列表
