## 基于netty和spring boot实现的分布式IM服务

包含server,route server,client demo

##### 应用依赖

zookeeper，redis

##### 功能列表

单聊，广播，消息记录

##### 测试

server

```properties
fire-im.server.zk-address=zookeeper地址,ip:port
fire-im.server.route-url=路由服务地址
fire-im.server.weight=当前机器的权重值,integer,路由策略为随机权重时使用
```

route

```properties
fire-im.route.zk-address=zookeeper地址,ip:port
fire-im.route.route-strategy=使用的路由策略(一致性hash/轮询/随机/权重随机/第一个/最后一个)
redis config
```

client

```properties
fire-im.client.route-url=路由服务地址
```

依次启动server,route和client
