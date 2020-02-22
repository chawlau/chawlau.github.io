# web站点和nginx
#### LB cluster
* scale up
* scale out: 水平扩展
* upstream server

#### session保持
* session绑定 sh 持久连接
* session集群 多播方式通讯
* session服务器：存储流式服务器 memcache redis

#### 公共缓存
* PCI-E SSD
* SATA 100
* SCSI 150
* SSD 300～500
* 并发是3万

#### 垂直拆分
* 分散写压力
* 数据库切片 

#### I/O
* 同步和异步 被调用者的是否立即返回
* 阻塞和非阻塞 调用者自己在收到相应之前是否自己挂起
![-w930](media/15412284008426/15412366723925.jpg)
 
* sendfile //TODO

#### cache loader
* 检查缓存存储的缓存对象
* 使用缓存元数据建立内存数据库
* key放内存，value放数据库

#### cache manager
* 缓存的失效过期以及检验，定时清理

#### nginx config
* main 对应全局属性
* event IO 模型
* http 如果处理http请求

```
  http {
    directive
    server {
      listen
      server_name
      location {
      
      }
    }
  }
```