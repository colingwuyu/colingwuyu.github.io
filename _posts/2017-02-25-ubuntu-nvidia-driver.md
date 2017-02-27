---
layout: post
title:  "Ubuntu N卡驱动安装"
date:   2017-02-25 
categories: Ubuntu
---
移除所有N卡相关的第三方驱动
{% highlight ruby %}
sudo apt-get remove nvidia*
sudo apt-get purge nvidia*
{% endhighlight %}

去除nouvea open source驱动

添加32位架构
{% highlight ruby %}
sudo dpkg --add-architecture i386
{% endhighlight %}

检查添加的32位架构
{% highlight ruby %}
dpkg --print-architecture
dpkg --print-foreign-architectures
{% endhighlight %}

下载N卡官网的Linux驱动

安装驱动前注销，在登录页面按Alt+Ctrl+F1进入tty关闭X server
{% highlight ruby %}
sudo service lightdm stop
{% endhighlight %}

安装驱动
{% highlight ruby %}
sudo sh <N-Driver>
{% endhighlight %}

重新启动X server
{% highlight ruby %}
sudo service lightdm start
{% endhighlight %}


安装完成！！ 
