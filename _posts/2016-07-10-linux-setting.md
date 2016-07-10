---
layout: post
title: Linuxでの日本語入力の文字化け対策
date: 2016-07-10
categories: linux
---

viなどで日本語を含むファイルを編集したり、日本語を書こうとすると、文字がウニウニと文字化けする。


原因として、環境変数が合っていないためで、環境変数を確認する`printenv`コマンドで確認する。


```
$ printenv | grep LANG
```


これで帰ってきた結果が、eucなりutf-8なり、希望する設定と違ったら、修正する必要があります。


言語関係の設定は

```
/etc/sysconfig/i18n
```

に書かれています。

このファイルを

```
LANG=ja_JP.utf-8
LC_ALL=ja_JP.utf-8
```

と書き換えて、ログインし直せばOKです。

