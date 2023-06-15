---
category: bash
date: 2023-06-15
---
1つのコマンドに対して複数の補完関数を擬似的に登録するというのが実現できた。

構造は単純で、1つ目の補完関数の中で補完するものがなければ1つ目の関数の最後で2つ目の補完関数を呼ぶ、というだけ。

## Ref

- https://github.com/sasaplus1/dotfiles/blob/a19443eb9c10b17a1855c0ca9c73e7e2982425e5/bash/.bashrc#L153-L214
