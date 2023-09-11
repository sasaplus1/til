---
category: bash
date: 2023-09-11
---
空のディレクトリを削除する方法を調べた。

```bash
$ find . -type d -empty -delete
```

削除する前に確認したければ`-delete`を`-print`にすると出力される。

カレントディレクトリ直下のディレクトリのみ削除したければ`-maxdepth`をつけると良い。

```bash
$ find . -maxdepth 1 -type d -empty -delete
```
