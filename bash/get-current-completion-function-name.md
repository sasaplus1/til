---
category: bash
date: 2023-06-12
---
コマンドに対して既に登録されている補完関数の名前を取得する方法を知った。

```bash
$ complete -p command 2>/dev/null | awk '/-F/ { print $(NF-1) }'
```

これで例えば、新しい補完関数を登録したいが古い補完関数も使用したい場合に再利用できる。（はず）
