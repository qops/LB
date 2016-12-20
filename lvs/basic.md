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
突破LVS瓶颈，LVS Cluster部署（OSPF + LVS） 
https://my.oschina.net/lxcong/blog/143904
```
