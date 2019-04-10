## Ansible

### 修改配置文件
```
/etc/ansible/ansible.cfg
host_key_checking = False
```

### 传输文件
```
ansible 172.16.0.9 -m copy -a "src=./basic.sh dest=/tmp/basic.sh mode=0755"
```

### 远程执行脚本
```
ansible 172.16.0.9 -m shell -a "/tmp/test.sh"
```