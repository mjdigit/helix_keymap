# helix_keymap
運指を少なくすることを目的に、下4行を中心に利用することを想定したキーマップです。

* Enter, Ctrl, Shift, GUI, App keyを一般的なキーボードに合わせて配置
* Space keyへのアクセスをよくするためにEISU, Lower, Raise, KANAを1key外側へ移動
* 日本語入力で多用する"-"をBase layerへ移動
* 誤打防止のためB, N keyをそれぞれ右手内側、左手内側へ配置
  - あと、距離の遠いこの位置にカッコを残しておきたくなかった
* Function, 数字, 一部記号keyはLower layerへまとめて移動
  - default keymapでLowerに居た記号はLower + Shiftで入力することを想定
* 移動キー, Del, BkspなどはRaise layer + 右手側のキーで入力できるように設定
  - 不在だったPrsc, Sclk, Pause, Insもこのlayerへ配置
  - カーソル移動はVim準拠とすることで指の移動を削減
  - 多用するBack Spaceは入力しやすいRaise + 右手小指に設定
* 滅多に使うことのないであろうAdjustはLower + Raiseで代用することを想定し削除

## Layout

### Qwerty

```
 ,-----------------------------------------.             ,-----------------------------------------.
 |   `  |   1  |   2  |   3  |   4  |   5  |             |   6  |   7  |   8  |   9  |   0  | Bksp |
 |------+------+------+------+------+------|             |------+------+------+------+------+------|
 | Esc  |   Q  |   W  |   E  |   R  |   T  |             |   Y  |   U  |   I  |   O  |   P  |  -   |
 |------+------+------+------+------+------|             |------+------+------+------+------+------|
 | Tab  |   A  |   S  |   D  |   F  |   G  |             |   H  |   J  |   K  |   L  |   ;  |Enter |
 |------+------+------+------+------+------+------+------+------+------+------+------+------+------|
 | Shift|   Z  |   X  |   C  |   V  |   B  |   N  |   B  |   N  |   M  |   ,  |   .  |   /  | Shift|
 |------+------+------+------+------+------+------+------+------+------+------+------+------+------|
 | Ctrl | Alt  | GUI  | EISU |Lower |Space |Space | Bksp |Space |Raise | KANA | Alt  | App  | Ctrl |
 `-------------------------------------------------------------------------------------------------'
```

### Lower
```
 ,-----------------------------------------.             ,-----------------------------------------.
 |   `  |   1  |   2  |   3  |   4  |   5  |             |   6  |   7  |   8  |   9  |   0  | Bksp |
 |------+------+------+------+------+------|             |------+------+------+------+------+------|
 |  F1  |  F2  |  F3  |  F4  |  F5  |  F6  |             |  F7  |  F8  |  F9  |  F10 |  F11 |  F12 |
 |------+------+------+------+------+------|             |------+------+------+------+------+------|
 |      |   1  |   2  |   3  |   4  |   5  |             |   6  |   7  |   8  |   9  |   0  |   =  |
 |------+------+------+------+------+------+------+------+------+------+------+------+------+------|
 |      | Bksp | Left | Down |  Up  |Right |      |      |   '  |   [  |   ]  |  \   |  `   |      |
 |------+------+------+------+------+------+------+------+------+------+------+------+------+------|
 |      |      |      |      |      |      |      | Del  |      |      |      |      |      |      |
 `-------------------------------------------------------------------------------------------------'
```

### Raise
```
 ,-----------------------------------------.             ,-----------------------------------------.
 |   ~  |   !  |   @  |   #  |   $  |   %  |             |   ^  |   &  |   *  |   (  |   )  | Del  |
 |------+------+------+------+------+------|             |------+------+------+------+------+------|
 |      | Mute | Vol- | Vol+ |      |      |             | Home |PageUp| Prsc | Sclk | Pause|      |
 |------+------+------+------+------+------|             |------+------+------+------+------+------|
 | Caps | Prev | Play | Next |      |      |             | Left | Down |  Up  |Right | Bksp |      |
 |------+------+------+------+------+------+------+------+------+------+------+------+------+------|
 |      |      |      |      |      |      |      |      | End  |PageDn| Del  |      | Ins  |      |
 |------+------+------+------+------+------+------+------+------+------+------+------+------+------|
 |      |      |      |      |      |      |      |      |      |      |      |      |      |      |
 `-------------------------------------------------------------------------------------------------'
```

### Adjust (Lower + Raise)
```
 ,-----------------------------------------.             ,-----------------------------------------.
 |  F1  |  F2  |  F3  |  F4  |  F5  |  F6  |             |  F7  |  F8  |  F9  |  F10 |  F11 |  F12 |
 |------+------+------+------+------+------|             |------+------+------+------+------+------|
 |      | Reset|RGBRST|      |      |      |             |      |      |      |      |      |  Del |
 |------+------+------+------+------+------|             |------+------+------+------+------+------|
 |      |      |      |Aud on|Audoff| Mac  |             | Win  |Qwerty|Colemk|Dvorak|      |      |
 |------+------+------+------+------+------+------+------+------+------+------+------+------+------|
 |      |      |      |      |      |      |      |      |      |      |RGB ON| HUE+ | SAT+ | VAL+ |
 |------+------+------+------+------+------+------+------+------+------+------+------+------+------|
 |      |      |      |      |      |      |      |      |      |      | MODE | HUE- | SAT- | VAL- |
 `-------------------------------------------------------------------------------------------------'
```

## How to build

1. 以下を参考にビルド環境を構築してください
  - https://github.com/MakotoKurauchi/helix/blob/master/Doc/firmware_jp.md
2. /keyboards/helix/rev2/keymaps/に https://github.com/mjdigit/helix_keymap.git をcloneしてください
3. 環境に応じてrules.mkを設定してください
4. `make helix:helix_keymap`でファームウェアをビルドします。そのままキーボードへ書き込みたい場合は`:avrdude`を付けます
5. ファームウェアを左右のキーボードに書き込んでください
