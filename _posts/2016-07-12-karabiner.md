---
layout: post
title: Karabinerを使ってvimのキーコンフィグに変更する
date: 2016-7-12
categories: mac
---

vimのキーコンフィグを覚えるために`Karabiner`というアプリを使ってデフォルトのキー操作をvimに変更してみました。

まず、初めは`Simple Vi Mode v2`だけをONにして、移動を`hjkl`でできるように設定ました。

慣れたら、`Ubiquitous Vim Bindings`を有効にしてその他のvimのキーコンフィグを設定する予定。

その他に設定したことは、_Key Repeat_ をはやく設定しました。

> Key Repeatとは
> ずっとキーを押してる時の入力速度のこと。  
> 例えば、矢印キーでの移動に関係してきます。
> これ、Windowsに比べて、macの場合、めっちゃ遅いです。


デフォルトでは、

```
Delay Until Repeat（500ms）
Key Repeat（83ms）
```

となっているところを、以下のように変更。

```
Delay Until Repeat（250ms）
Key Repeat（53ms）
```
