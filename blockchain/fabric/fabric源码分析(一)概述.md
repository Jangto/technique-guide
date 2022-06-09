

## fabric2.2.0源码目录的基本结构     
* bcssp：与密码学（加密、签名、证书等）相关的加密服务代码目录，将Fabric中用到的密码学相关的函数抽象成了一组接口，便于拓展
* ci：
* cmd：类似于提供了一个客户端，可以通过命令和Fabric交互
* common：一些公共库，主要是相关的错误处理、日志处理、账本存储、策略以及各种工具等。比较复杂，在后面代码分析遇到时逐一分析
* core：Fabric的组件的核心模块，每一个组件都有一个子目录（chaincode:与智能合约相关，comm:与网络通信相关，endorser:与背书节点相关）
* discovery：客户端及相关服务的支持
* docs：以.rst文件为核心，可编译生成文档。说明文档的目录
* devenv：Fabric 官方提供的开发环境，使用的是Vagrant
* events：事件监听机制
* gossip：组织内部节点数据同步的通信协议，有一定容错能力且可达到最终一致的传播算法，用于组织内部数据同步
* idemix：对IDEMIX的支持相关，和零知识证明相关，适用于开发环境
* images：Docker镜像打包文件，Docker镜像都是通过这个目录下的配置文件生成的
* integration：行为驱动开发相关
* internal：
* msp：成员服务管理，在Fabric网络中会为每一个成员提供相应的证书，msp用来验证管理在节点间通信的证书，不同的通道通过msp划分
* orderer：排序节点的相关模块，orderer是区域链中的专用名词，用于消息的订阅与分发处理，用于处理区块的打包处理
* peer：peer节点的入口，节点管理的模块，包括通道、链码等
* pkg：
* protos：定义Fabric中的数据结构和数据服务，包括定义相关的通信协议数据处理（protobuf）文件和生成的 go 文件
* protoutil：原型目录，定义个各种原型和生成的对应的XXX.pb.go源码
* release：发布模板
* release_notes：基础的配置文件例子
* sampleconfig：基础的配置文件例子
* scripts：相关应用服务的脚本,早期版本将例程放在 examples下，后续版本，合并在script文件夹里
* tools：
* vagrant：
* vendor：原意是商贩，此处存放Go中使用的第三方包

参考
[Fabric开发（四）Fabric源码赏析](https://blog.csdn.net/jambeau/article/details/107687446)
[Fabric 源码解析——源码目录解析](https://dandelioncloud.cn/article/details/1504318261805281282)
