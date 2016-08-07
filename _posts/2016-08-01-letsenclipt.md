---
layout: post
title: 無料で証明書を取得し、HTTPSを実現する(Let’s Encrypt)
date: 2016-08-01
categories: linux
---


証明書を取得する前提として、ドメインを取得する必要があります。
現在、無料でもドメイン名を取得できるサービスが多くあり、ダイナミックDNSを利用することが主流だと思います。
しかし、私の場合Let’s Encryptで証明書を取得する際、エラー（このドメインから多くの証明書が発行されていて、もう無理です的な）がでて、取得できませんでした。

そこで、私が現在使用しているルータ（aterm）の機能、ホームIPロケーション機能を利用して、ドメインを取得しました。

詳しくは[こちら](http://www.aterm.jp/function/guide17/list-data/common/main/8600/m01_m72.html)を参照。


HTTPSの導入は例のごとく[ここ](https://centossrv.com/apache-certbot.shtml)を参照。
