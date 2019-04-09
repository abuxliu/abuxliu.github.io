## 网络测试笔记
### Listen一个端口（可以接数据）
> apt install nmap

```
nping --es --nc --ep 55672 -e eth0
```

### 占用一个端口
```
nc -lk 55672
```

### 抓包
```
tcpdump -i eth0 tcp dst port 55672 -w lab.pcap -v
```
