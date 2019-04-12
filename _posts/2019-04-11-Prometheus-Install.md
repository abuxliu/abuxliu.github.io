## Prometheus-Install
> 代码千万行，网络第一行

### 零、版本要求
|模块|版本|备注|
|:---:|:---:|:---:|
|Go|1.11.4||
|Prometheus|2.6.0||
|Grafana|5.4.2||

### 一、部署Go
```
wget https://dl.google.com/go/go1.11.4.linux-amd64.tar.gz
tar -C /opt/ -xzf go1.11.4.linux-amd64.tar.gz
echo "export PATH=$PATH:/opt/go/bin" >> /etc/profile
echo "PATH=$PATH:/opt/go/bin" >> /etc/environment
source /etc/profile
source /etc/environment
go version
```

### 二、部署Prometheus
```
wget https://github.com/prometheus/prometheus/releases/download/v2.6.0/prometheus-2.6.0.linux-amd64.tar.gz
tar -C /opt/ -xzf prometheus-2.6.0.linux-amd64.tar.gz
cd /opt/prometheus-2.6.0.linux-amd64
sed -i "s/localhost/0.0.0.0/g" prometheus.yml
nohup ./prometheus  --config.file=prometheus.yml &
lsof -i :9090
```

### 三、部署Grafana
```
wget https://dl.grafana.com/oss/release/grafana-5.4.2.linux-amd64.tar.gz
tar -C /opt/ -xzf grafana-5.4.2.linux-amd64.tar.gz
# modify 环境变量 配置文件
```

### 参考资料
[监控神器普罗米修斯Prometheus安装配置](https://blog.csdn.net/ywd1992/article/details/85989259)
