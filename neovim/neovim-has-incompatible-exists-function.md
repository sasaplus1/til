---
category: neovim
date: 2023-07-14
---
Neovimの `exists()` 関数は `?funcname` の形式に対応していないというのを知った。

Vimを使うことを前提とした `.vimrc` を書いていたので、面倒ではあるが以下のような書き方にした。

```vim
exists('?funcname') || (has('nvim') && exists('*funcname'))
```
