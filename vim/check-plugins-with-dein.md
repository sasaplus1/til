---
category: vim
date: 2023-09-11
---
dein.vimで使用していないプラグインを削除する方法について調べた。

```vim
:call map(dein#check_clean(), "delete(v:val, 'rf')")
:call dein#recache_runtimepath()
```

他にプラグインに対して`lazy`の指定があるが指定している意味がないプラグインを検出する関数などがある。

```vim
:echo dein#check_lazy_plugins()
```

## Ref

- https://hodalog.com/how-to-remove-plugin-using-dein/
