---
layout:     post
title:      "GoogleImg"
subtitle:   "NginxGoogleMod"
date:       2018-11-18 12:00:00
author:     "ABU"
header-img: "img/post-bg-2015.jpg"
catalog: false
tags:
    - 杭州商学院
---

写在前面的话
>Nginx Mod Google

####DownLoad Addr:
```
http://us.abu.pub/files/googleImg.bz2
```

####Shell CMD:
```
tar -xjvf googleImg.bz2
docker load -i googleImg.tar
docker run -itd -p 81:80 -h google_img --name google_img google_img /bin/bash
docker attach google_img
	/opt/nginx-1.7.8/sbin/nginx
	ctrl+p+q
curl -I localhost:81
```
