---
layout: post
title:  "ファイル比較"
date:   2016-08-01
categories: ruby 
---

2つのファイルが同一かどうか比較する方法。ruby には
 `FileUtils#compare_file` メソッドがある。 [マニュアル][ruby-docs] を調
べてみる。

{% highlight ruby %}
$ pry
[1] pry(main)> require 'fileutils'
[2] pry(main)> show-sourse FileUtils#compare_file
{% endhighlight %}

このメソッドは引数を2つ取る。引数はファイル名が入る。2つのファイルのサイズが等しければcompare_streamメソッドで2つのファイルの内容を比較する。

Digestを使ってハッシュ値をとったりするのかと思っていたが、ファイルの内
容が一致するかどうかを知りたいのだから、これで理にかなっている。

compare_stream 
[ruby-docs]: http://docs.ruby-lang.org/ja/2.1.0/class/FileUtils.html#M_CMP
