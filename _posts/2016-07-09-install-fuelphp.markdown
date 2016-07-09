---
layout: post
title:  "Installing FuelPHP"
date:   2016-07-09
categories: PHP
---
NetBSDにFuelPHPをインストールしたときのメモ。

{% highlight shell %}
$ su -
$ cd /usr/pkgsrc/converter/php-json
$ sudo bmake package-install clean
$ sudo vi /usr/pkg/etc/php.ini      # add 'extensions=jso.so'
$ curl get.fuelphp.com/oil | sh
$ sudo vi /usr/local/bin/oil   # edit bash path(#!/usr/p@kg/bin/bash)
$ oil create name_of_application
{% endhighlight %}

gitリポジトリを設定

{% highlight shell %}
$ cd name_of_application
$ git init
$ git add -A
$ git commit -m 'initial commit'
$ git remote add origin path_of_bare_repository
$ git push --set-upstream origin master
{% endhighlight %}
