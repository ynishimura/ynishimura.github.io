---
layout: post
title: VimFilerの操作
date: 2016-08-01
categories: linux vim
---


[vimfilerの基本操作](http://qiita.com/0829/items/261225a51439776b36bf)

[vimfilerの応用](http://www.karakaram.com/vimfiler#example)

```

nnoremap <Space>e :VimFilerExplore -split -winwidth=30 -find -no-quit<Cr>



◆現在のキーマップ

"unite prefix key.
nnoremap [unite] <Nop>
nmap <Space>u [unite]

" unite.vim keymap
let g:unite_source_history_yank_enable =1
nnoremap <silent> [unite]u :<C-u>Unite<Space>file<CR>
nnoremap <silent> [unite]g :<C-u>Unite<Space>grep<CR>
nnoremap <silent> [unite]f :<C-u>Unite<Space>buffer<CR>
nnoremap <silent> [unite]b :<C-u>Unite<Space>bookmark<CR>
nnoremap <silent> [unite]a :<C-u>UniteBookmarkAdd<CR>
nnoremap <silent> [unite]m :<C-u>Unite<Space>file_mru<CR>
nnoremap <silent> [unite]h :<C-u>Unite<Space>history/yank<CR>
nnoremap <silent> [unite]r :<C-u>Unite -buffer-name=register register<CR>
nnoremap <silent> [unite]c :<C-u>UniteWithBufferDir -buffer-name=files file<CR>
```