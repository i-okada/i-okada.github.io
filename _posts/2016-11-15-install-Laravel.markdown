---
layout: post
title:  "Installing Laravel"
date:   2016-11-15
categories: php
---
WindowsにLaravel(version: )をインストールしたときのメモ。

## 手順

### composer インストール

{% highlight shell %}
$ curl -sS https://getcomposer.org/installer | php
$ sudo mv composer.phar /usr/local/bin/composer
{% endhighlight %}

### Laravel インストール

{% highlight shell %}
$ composer global require "laravel/installer=~1.1"
{% endhighlight %}

### Laravel プロジェクト生成

{% highlight shell %}
$ composer create-project laravel/laravel project_name
{% endhighlight %}
