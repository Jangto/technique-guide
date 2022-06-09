

## fabric2.2.0源码目录的基本结构     
* bcssp：加密服务代码目录
* ci：
* cmd：类似于提供了一个客户端，可以通过命令和Fabric交互
* common：全局公用代码目录，主要是相关的日志、错误、工具等。比较复杂，在后面代码分析遇到时逐一分析。
* core：核心功能代码目录，Fabric的相关核心模块，包括背书、链码等
* discovery：客户端及相关服务的支持
* docs：以.rst文件为核心，可编译生成文档。说明文档的目录
* gossip：本意是绯闻的意思，是一种可达到去中心化，有一定容错能力且可达到最终一致的传播算法
* idemix：对IDEMIX的支持相关，和零知识证明相关，适用于开发环境
* images：打包文件
* integration：行为驱动开发相关
* internal：
* msp：成员服务管理,用来验证管理在节点间通信的证书，不同的通道通过msp划分
* orderer：排序节点的相关模块，orderer是区域链中的专用名词，用于消息的订阅与分发处理，用于处理区块的打包处理
* peer：节点管理的模块，包括通道、链码等
* pkg：
* protos：相关的通信协议数据处理（protobuf）以及数据结构体
* protoutil：原型目录，定义个各种原型和生成的对应的XXX.pb.go源码
* release：发布模板
* release_notes：基础的配置文件例子
* sampleconfig：基础的配置文件例子
* scripts：相关应用服务的脚本,早期版本将例程放在 examples下，后续版本，合并在script文件夹里
* tools：
* vagrant：
* vendor：原意是商贩，此处是存放用到Go的相关的第三方库包

  
[Fabric开发（四）Fabric源码赏析](https://blog.csdn.net/jambeau/article/details/107687446)
