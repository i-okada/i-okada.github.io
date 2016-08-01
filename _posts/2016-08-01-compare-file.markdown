---
layout: post
title:  "ファイル比較"
date:   2016-08-01
categories: ruby 
---

学生の提出物を採点するときに、提出物が誰か他の学生のファイルをコピーし
たものかどうか調べる必要があります。それで、2つのファイルが同一かどう
か比較する方法について調べました。

ruby には `FileUtils#compare_file` メソッドがあります。
 [FileUtils.html][ruby-docs] のマニュアルを調べてみます。

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
