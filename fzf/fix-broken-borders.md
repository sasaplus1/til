---
category: fzf
date: 2023-08-30
---
fzfの描画する枠線がいつからか崩れるようになり、気になっていた。

ver.0.36.0から枠線の描画について変更があったらしく、それで特定の環境では崩れていたらしい。

`RUNEWIDTH_EASTASIAN`の環境変数に`0`を指定することで表示崩れが修正できた。

## Ref

- https://twitter.com/hayajo/status/1696724625999483295
- https://twitter.com/hayajo/status/1625846313060548609
- https://github.com/junegunn/fzf/releases/tag/0.36.0
