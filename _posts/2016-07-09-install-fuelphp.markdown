---
layout: post
title:  "Installing FuelPHP"
date:   2016-07-09
categories: PHP
---
NetBSDにFuelPHPをインストールしたときのメモ。

{% highlight shell %}
$ su -
# cd /usr/pkgsrc/converter/php-json
# bmake package-install clean
# vi /usr/pkg/etc/php.ini      # add 'extensions=jso.so'
# exit
$ curl get.fuelphp.com/oil | sh
$ sudo vi /usr/local/bin/oil   # edit bash path(#!/usr/p@kg/bin/bash)
$ oil create name_of_application
{% endhighlight %}
