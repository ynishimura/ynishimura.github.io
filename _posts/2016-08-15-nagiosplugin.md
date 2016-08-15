---
layout: post
title: nagiosにグラフのプラグインを導入
date: 2016-08-15
categories: linux nagios
---

### PNPをインストール

```
RPMforgeリポジトリ導入(RPMforge)を参照してRPMforgeリポジトリを導入する

[root@centos ~]# yum -y install rrdtool php-gd　←　PNPに必要なパッケージインストール

[root@centos ~]# /etc/rc.d/init.d/httpd reload　←　Apache設定再読み込み
httpd を再読み込み中:                                      [  OK  ]

[root@centos ~]#  wget https://sourceforge.net/projects/pnp4nagios/files/PNP-0.6/pnp4nagios-0.6.25.tar.gz　←　PNPダウンロード


[root@centos ~]# tar zxvf pnp-0.6.25.tar.gz　←　PNP展開

[root@centos ~]# cd pnp-0.6.25　←　PNP展開先ディレクトリへ移動

[root@centos pnp-0.6.25]# ./configure && make all && make install && make install-config　←　PNPインストール



完了後下記のログを出力する

*** PNP4Nagios sample config files installed ***

Please run 'make install-init' if you want to use
BULK Mode with NPCD



[root@centos pnp-0.6.25]# cd　←　PNP展開先ディレクトリを抜ける

[root@centos ~]# rm -rf pnp-0.6.25　←　PNP展開先ディレクトリを削除

[root@centos ~]# rm -f pnp-0.6.25.tar.gz　←　ダウンロードしたファイルを削除

```




### PNPインストール時のトラブルシューティング

./configure && make all && make install && make install-configのときに

Time/HiRes.pmのエラーがでたため


```
yum install perl-Time-HiRes

を実行すると問題なく通る
```


うまくいかないたまめ再度[ここのサイト](http://blog.redbox.ne.jp/pnp4nagios-install.html)をみてやりなおしてみる
