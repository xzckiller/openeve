## KeyboardLayout ##
eve\_qwerty.kl is loaded at boot time by system\_server process **at once**.
thats why It is just simple text.

KeyboardLayout contains SCANCODE KEYCODE mappings. like as

```
key 115   VOLUME_UP         WAKE
key 114   VOLUME_DOWN       WAKE
key 116   POWER             WAKE
key 14    DEL               WAKE_DROPPED
key 212   CAMERA
key 242   FOCUS
key 16    Q
key 17    W
key 18    E
key 19    R
key 20    T
key 21    Y
key 22    U
key 23    I
key 24    O
key 25    P
```
You can change `*.kl` files more easily but It is **not recommended** to do that.
If you change A<=>Q by `*.kl` it effects all other `*.kcm` files and make some `*.kcm` useless.

But you can change some keyboard behavior at `SCANCODE` level. you can change `HOME<=>BACK`, `ALT<=>SHIFT` etc.

## KeyboardMapping ##
It is more flexiable format.  `*.kcm` is loaded by applications.

It is provided as binary format.
It is loaded by every apps and that's why it is compiled binary.

KeyboardMapping contains several `KEYCODE` and `MODIFIERS` mapping combinations.
the part of `eve_qwerty.kcm` source shown below
```
[type=QWERTY]
# keycode      Display   Number    Base      Shift     Alt       Shift+Alt
0              '0'       '0'       '0'       ')'       ')'       ')'
1              '1'       '1'       '1'       '!'       '!'       '!'
2              '2'       '2'       '2'       '@'       '@'       '@'
3              '3'       '3'       '3'       '#'       '#'       '#'
4              '4'       '4'       '4'       '$'       '$'       '$'
5              '5'       '5'       '5'       '%'       '%'       '%'
...
D              'D'       '3'       'd'       'D'       ';'       0x04
E              'E'       '3'       'e'       'E'       'e'       0x301
F              'F'       '3'       'f'       'F'       '['       0xA5
...
COMMA          ','       ','       ','       ';'       ';'       '|'
# 0x1B =ESCAPE
PERIOD         '.'       '.'       '.'       0x1B      '?'       0x2026
TAB            0x9       0x9       0x9       0x9       0x9       0x9
SPACE          0x20      0x20      0x20      0x20      0xEF01    0xEF01
ENTER          0xA       0xA       0xA       0xA       0xA       0xA
```

`*.kcm.bin` is able to decompile by unkcm.
  * https://github.com/asedeno/unkcm
and `*.kcm.bin` is compiled by kcm.
  * http://forum.xda-developers.com/showpost.php?p=9208893&postcount=31