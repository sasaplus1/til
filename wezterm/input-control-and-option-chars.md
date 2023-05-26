---
category: wezterm
date: 2023-05-25
---
WezTermでIMEでの入力中に装飾キー付きの入力をしようとすると意図した入力にならないことに気がついた。

例えばIMEでの入力中に`control-h`で1文字削除しようとすると、IMEで入力中の文字が削除されるのでなくてIMEで入力を始めた位置から1文字削除されてしまったり。

他には`option-;`で`…`を入力することはできるのだけど、IMEで入力を始めた位置に挿入されてしまったり。

これは`macos_forward_to_ime_modifier_mask = "ALT|CTRL|SHIFT"`とすることで挙動を変更することができた。

IMEへ装飾キー付きのキー入力を送信するかどうかをこのオプションで指定できるらしくて、ここに`ALT`と`CTRL`がデフォルトでは指定されていないのでIMEを通らずにターミナルへ送信されていたみたいだった。

## Ref

- https://github.com/wez/wezterm/pull/2435
- https://github.com/wez/wezterm/pull/2435#issuecomment-1491290065
- https://wezfurlong.org/wezterm/config/lua/config/macos_forward_to_ime_modifier_mask.html
