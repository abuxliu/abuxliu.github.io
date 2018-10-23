---
layout:     post
title:      "学习问题排错集锦"
subtitle:   "这个冬天，谁陪我过？"
date:       2018-10-19 10:00:00
author:     "ABU"
header-img: "img/post-bg-2015.jpg"
catalog: false
tags:
    - 杭州商学院
---

写在前面的话
>把查到的资料记录下来，好记性不如烂笔头。

问题1：JAVA中使用nextLine()，没有输入就自动跳过

```
解决方案：
在nextInt();后的nextLine();会接收"\n"的问题，可以在他们中间加一个in.nextLine();语句来接收这个"\n"。
```

参考文档
>[JAVA中使用nextLine()，没有输入就自动跳过](https://www.cnblogs.com/1020182600HENG/p/6564795.html)<br>
>Thanks ABU

问题2：JAVA中判断两个字符串是否相等

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
>[JAVA中判断两个字符串是否相等](https://www.cnblogs.com/zhmt/archive/2011/09/12/2174210.html)<br>
>Thanks ABU

问题3：Sublime Text 3中文乱码问题解决

```
解决方案：
Sublime Text 3是我MacBook Pro最喜欢的代码编辑器，没有之一，因为她的性感高亮代码配色，更因为它的小巧，但是它默认不支持GBK的编码格式，因此打开GBK的代码文件，如果里面有中文的话，就会乱码
第一步：安装Package Control

大家如果是在官网下载的Sublime Text 3，那么首先需要安装一个

Package Control包，这是一个用来安装其他插件的包，不管装什么插件，首先要先装这个包才行；

安装Sublime Package Control非常简单。

1、打开Preferences菜单，并选择 Browse Packages…

2、系统会打开Sublime Text 3的Packages文件夹，回到上一级菜单，然后打开Installed Packages文件夹

3、下载并将下载的Package Control.sublime-package拷贝到Installed Packages文件夹(注意此处是Installed Packages，不是Packages文件夹)，这个如果不知道怎么下载的拷贝名字直接百度，第一个就是下载链接

4、重启Sublime Text 3
第二步：安装插件ConvertToUTF8和Codecs33

这两个插件才是解决乱码的重点，网上写了很多都是没有Codecs33这个插件，最新的其实不装这个插件还是不能解决全部乱码，还有乱码存在；在perferences选项一栏下面有个Package Control，点击Package Control，上面会出来一个输入框，我们输入install，就会自动有提示那个install package，我们点击一下install package，输入框会消失，稍等一下又会弹出个输入框。这时我们可以输入需要安装的插件包（ConvertToUTF8和Codecs33）了（一个装完安装第二步再装第二个），安装两个都成功后再重启打开就没有中文乱码了。
--------------------- 
作者：御前提笔小书童 
来源：CSDN 
原文：https://blog.csdn.net/qq_22260641/article/details/70666960 
版权声明：本文为博主原创文章，转载请附上博文链接！

```

参考文档
>[Sublime Text 3中文乱码问题解决](https://blog.csdn.net/qq_22260641/article/details/70666960)<br>
>Thanks ABU