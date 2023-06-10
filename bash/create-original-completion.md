---
category: bash
date: 2023-06-10
---
補完関数を自身で記述すれば好きなように入力補完ができることがわかった。

`complete` コマンドで特定のコマンドに対しての補完の設定ができる。
関数による補完の際には `compgen` コマンドを使用すると入力された値から候補を絞る出力が受け取れる。

## Ref

- https://tylerthrailkill.com/2019-01-19/writing-bash-completion-script-with-subcommands/
- https://tldp.org/LDP/abs/html/tabexpansion.html
