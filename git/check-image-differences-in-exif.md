---
category: git
date: 2023-06-15
---
`.gitattributes` について調べていて、設定次第では画像の差分をEXIFから確認できることを知った。

[ExifTool](https://exiftool.org/)をインストールして、 `.gitattributes` に以下のように記述する。

```gitconfig
*.png diff=exif
```

そして、Gitの設定を変更する。

```bash
$ git config diff.exif.textconv exiftool
```

これで画像に変更があった場合、EXIFの差分が確認できるらしい。

画像以外にもdocxのファイルに然るべきフィルターとなるコマンドを渡せば文字列の差分が表示できるそうなので、
テキストベースでないファイルであってもフィルターするコマンドがあれば差分を確認できるということになる。

## Ref

- https://git-scm.com/book/ja/v2/Git-%E3%81%AE%E3%82%AB%E3%82%B9%E3%82%BF%E3%83%9E%E3%82%A4%E3%82%BA-Git-%E3%81%AE%E5%B1%9E%E6%80%A7
- https://exiftool.org/
