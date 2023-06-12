---
category: gh
date: 2023-06-12
---
`gh` コマンドは標準出力をパイプするとカラーリングのない出力になるけど、これをパイプしてもカラーリングして出力する方法について調べた。

> CLICOLOR_FORCE: set to a value other than "0" to keep ANSI colors in output even when the output is piped.
> 
> GH_FORCE_TTY: set to any value to force terminal-style output even when the output is redirected. When the value is a number, it is interpreted as the number of columns available in the viewport. When the value is a percentage, it will be applied against the number of columns available in the current viewport.

カラーリングの出力だけであれば `CLICOLOR_FORCE` を環境変数で指定するので良さそう。

カラーリングだけでなくレイアウトもそのままに出力してほしかったので今回は `GH_FORCE_TTY` を使った。

## Ref

- https://cli.github.com/manual/gh_help_environment
