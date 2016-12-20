# lvs 的模式

### DR 直接路由
```
支撑后端real server 100台左右
```

### NAT 地址转换
```
后端real server 10台左右，如果这种方式不如用nginx
```

### Tunnel 隧道
```
director与real server不在一个机房
```

### lvs-fullnat（双向转换）
```
ali
```

### lvs+ospf(等价多路径)
```
突破LVS瓶颈，LVS Cluster部署（OSPF + LVS）  https://my.oschina.net/lxcong/blog/143904
http://noops.me/?p=974
```


#### ospf等价多路径
ECMP（Equal-CostMultipathRouting）等价多路径，存在多条不同链路到达同一目的地址的网络环境中，如果使用传统的路由技术，发往该目的地址的数据包只能利用其中的一条链路，其它链路处于备份状态或无效状态，并且在动态路由环境下相互的切换需要一定时间，而等值多路径路由协议可以在该网络环境下同时使用多条链路，不仅增加了传输带宽，并且可以无时延无丢包地备份失效链路的数据传输。
