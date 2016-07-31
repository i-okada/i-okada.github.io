---
layout: post
title:  "Installing phpldapadmin"
date:   2016-07-31
categories: LDAP
---

NetBSDにphpldapadminをインストールしたときのメモ。なお、apacheではなく、
nginxで動かしている。

{% highlight shell %}
$ cd /usr/pkgsrc/database/phpldapadmin
$ sudo bmake package-install clean
$ su -
# cd /usr/pkg/share/nginx/html ; ln -s /usr/pkg/share/phpldapadmin/htdocs phpldapadmin
{% endhighlight %}

ブラウザで http://localhost/phpldapadmin/ にアクセスして動作確認。
