## Microsoft Learn
> 用户名：abuxliu
> 
> 账号：rhcals@163.com

### 云存储需求
1. 可靠：自动备份，灾难恢复
2. 安全：高强度的访问控制
3. 方便：提供多种连接方式，并且支持作为块设备连接
4. 扩展性：随时扩展容量
5. 成本效益：运营成本（价格即用即付），运维成本（零）

### 将Blob存储挂载到Linux服务器
[参考资料1: 如何使用 Blobfuse 将 Blob 存储装载为文件系统（Global）](https://docs.microsoft.com/zh-cn/azure/storage/blobs/storage-how-to-mount-container-linux)

[参考资料2: 如何使用 Blobfuse 将 Blob 存储装载为文件系统（China）](https://docs.azure.cn/zh-cn/articles/azure-operations-guide/storage/aog-storage-blob-howto-mount-as-file-system-via-blobfuse)

#### 1. 确认操作系统版本
```
lsb_release -a
```
#### 2. 安装驱动程序
```
wget https://packages.microsoft.com/config/ubuntu/16.04/packages-microsoft-prod.deb
dpkg -i packages-microsoft-prod.deb
apt-get update
apt-get install blobfuse
```

#### 3. 准备装载
> Blobfuse 要求文件系统中存在一个临时路径，用于缓冲和缓存任何打开的文件，以便提供类似本机的性能。 对于此临时路径，请选择性能最高的磁盘，或者使用 ramdisk 来获得最佳性能。
> 
> 将 SSD 用作临时路径：在 Azure 中，可以使用 VM 上提供的临时磁盘 (SSD)，为 Blobfuse 提供低延迟缓冲区。 在 Ubuntu 发行版中，此临时磁盘装载在“/mnt”上。 在 Red Hat 和 CentOS 发行版中，此临时磁盘装载在“/mnt/resource/”上。

```
mkdir /mnt/blobfusetmp
# chown <youruser> /mnt/blobfusetmp
touch /etc/fuse_connection.cfg
cat > /etc/fuse_connection.cfg << EOF
accountName ilsvideo
accountKey L==
containerName videofile
blobEndpoint ilsvideo.blob.core.chinacloudapi.cn
EOF
chmod 700 /etc/fuse_connection.cfg
mkdir /data
```

#### 4. 装载Blob容器
>  装载该目录的用户是可以访问它的唯一人员，默认情况下，这可以保护访问权限。 若要允许所有用户进行访问，可以通过选项 -o allow_other 进行装载。

```
blobfuse /data --tmp-path=/mnt/blobfusetmp  --config-file=/etc/fuse_connection.cfg --use-https=true --file-cache-timeout-in-seconds=0 -o allow_other
```

