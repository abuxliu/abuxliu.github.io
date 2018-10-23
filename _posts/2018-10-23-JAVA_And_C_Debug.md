---
layout:     post
title:      "程序设计问题集锦"
subtitle:   "这个冬天，你陪我过"
date:       2018-10-23 10:00:00
author:     "ABU"
header-img: "img/post-bg-2015.jpg"
catalog: true
tags:
    - 杭州商学院
---

#程序设计语言疑难点集锦
##写在前面的话
>把查到的资料记录下来，好记性不如烂笔头。

###问题1：JAVA中使用nextLine()，没有输入就自动跳过
```
解决方案：
在nextInt();后的nextLine();会接收"\n"的问题，可以在他们中间加一个in.nextLine();语句来接收这个"\n"。
```
参考文档
>>[JAVA中使用nextLine()，没有输入就自动跳过](https://www.cnblogs.com/1020182600HENG/p/6564795.html)<br>
>>Thanks ABU

###问题2：JAVA中判断两个字符串是否相等
```
解决方案：
A字符串和B和字符串比较:
if(A.equals(B)){
}
返回true 或false.
String 的equals 方法用于比较两个字符串是否相等。由于字符串是对象类型，所以不能用简单的“==”判断。而使用equals比较两个对象的内容是否相等。
注意：
equals()比较的是对象的内容（区分字母的大小写格式），但是如果使用“==”比较两个对象时，比较的是两个对象的内存地址，所以不相等。即使它们内容相等，但是不同对象的内存地址也是不相同的。
```
参考文档
>>[JAVA中判断两个字符串是否相等](https://www.cnblogs.com/zhmt/archive/2011/09/12/2174210.html)<br>
>>Thanks ABU