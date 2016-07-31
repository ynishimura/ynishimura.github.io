---
layout: post
title: apache で　phpを動かすときに500のエラーが出た時の対処
date: 2016-08-01
categories: php linux apache
---


### apache でphpを動かす

apacheでphpを動かそうと思い、apacheの設定でつまずいたのでメモ


phpのコンテンツにアクセスすると500のエラが表示される

まず、`エラーログ`をみる。私の場合下記のエラが出力されていた

```
[Sat Jul 30 02:15:27 2016] [error] [client 127.0.0.1] Premature end of script headers: index.php
[Sat Jul 30 02:25:27 2016] [error] [client 127.0.0.1] (8)Exec format error: exec of '/var/www/html/index.php' failed
```

上記のエラーが出た際の確認ポイント（httpd.confの確認）

```
・ScriptAliasをコメントアウトする

・AddHandler cgi-script .cgi .pl .phpを変更して、AddHandler cgi-script .cgi

私の場合、phpファイルがcgiと認識されていたのが原因らしい

```