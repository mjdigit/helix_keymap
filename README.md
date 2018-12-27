# helix_keymap
Prototype Helix keymap currently supports only 5-rows.

Please refer following to know how to build the keymap.

https://github.com/MakotoKurauchi/helix/blob/master/Doc/firmware_jp.md

運指を少なくすることを目的に、一部Vortex Coreのキーマップを参考にして作成したキーマップです。
基本的に使用するのは下4行になるようにしています。
使用感をしばらく確認した後に4行版へも展開していこうと考えています。


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
 |   1  |   2  |   3  |   4  |   5  |   6  |             |   7  |   8  |   9  |   0  |   -  |   =  |
 |------+------+------+------+------+------+------+------+------+------+------+------+------+------|
 |      |      |      |      |      |      |      |      |   '  |   [  |   ]  |  \   |  `   |      |
 |------+------+------+------+------+------+------+------+------+------+------+------+------+------|
 |      |      |      |      |      |      |      |      |      |      |      |      |      |      |
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
 |      |      |      |      |      |      |      | Del  |      |      |      |      |      |      |
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