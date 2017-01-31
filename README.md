# Firmware


## Edit Keymap

```sh
gedit ~/Git/Firmware/qmk/keyboards/ergodox/ez/keymaps/dawkiny/keymap.c
~/Git/Firmware/qmk/keyboards/ergodox/make ez dawkiny

~/Git/Firmware/teensy/teensy.64bit &
```

![make_and_teensy](https://github.com/dawkiny/Firmware/edit/master/make_and_teensy.png)
<p align="center">
  <img src="https://github.com/dawkiny/Firmware/edit/master/make_and_teensy.png" width="350"/>
</p>
---


## Layers
```
/* Keymap 0: Basic layer
 *
 * ┌───────┬─────┬─────┬─────┬─────┬─────┬─────┐     ┌─────┬─────┬─────┬─────┬─────┬─────┬───────┐
 * │  Esc  │  1  │  2  │  3  │  4  │  5  │CtFn5│     │  6  │  7  │  8  │  9  │  0  │  -  │   +   │
 * ├───────┼─────┼─────┼─────┼─────┼─────┼─────┤     ├─────┼─────┼─────┼─────┼─────┼─────┼───────┤
 * │  Tab  │  Q  │  W  │  E  │  R  │  T  │  <- │     │ Ctl │  Y  │  U  │  I  │  O  │  P  │   \   │
 * ├───────┼─────┼─────┼─────┼─────┼─────┤  =  │     │ Ent ├─────┼─────┼─────┼─────┼─────┼───────┤
 * │   ~   │  A  │  S  │  D  │  F  │  G  ├─────┤     ├─────┤  H  │  J  │  K  │  L  │  ;  │   '   │
 * ├───────┼─────┼─────┼─────┼─────┼─────┤ Tg  │     │ Ctl ├─────┼─────┼─────┼─────┼─────┼───────┤
 * │ LSHFT │  Z  │  X  │  C  │  V  │  B  │ Npd │     │ Fn5 │  N  │  M  │  ,  │  .  │  /  │ Shift │
 * └─┬─────┼─────┼─────┼─────┼─────┼─────┴─────┘     └─────┴─────┼─────┼─────┼─────┼─────┼─────┬─┘
 *   │ CTL │CtAlt│Wn/Cd│ App │ ALT │                             │ RAt │ RCl │  [  │  ]  │ TgM │
 *   └─────┴─────┴─────┴─────┴─────┘ ┌─────┬─────┐ ┌─────┬─────┐ └─────┴─────┴─────┴─────┴─────┘
 *                                   │ Lft │ Rgt │ │ Lft │ Rgt │
 *                             ┌─────┼─────┼─────┤ ├─────┼─────┼─────┐
 *                             │     │     │ SHm │ │ Up  │     │     │
 *                             │ Spc │ Bsp ├─────┤ ├─────┤ Del │ Ent │
 *                             │     │     │ SEd │ │ Dwn │     │     │
 *                             └─────┴─────┴─────┘ └─────┴─────┴─────┘
 */
/* Keymap 1: Numpad Layer
 * ┌───────┬─────┬─────┬─────┬─────┬─────┬─────┐     ┌─────┬─────┬─────┬─────┬─────┬─────┬───────┐
 * │  Ver  │ Fn1 │ Fn2 │ Fn3 │ Fn4 │ Fn5 │ Fn6 │     │ Fn7 │ Fn8 │ Fn9 │ F10 │ F11 │ F12 │       │
 * ├───────┼─────┼─────┼─────┼─────┼─────┼─────┤     ├─────┼─────┼─────┼─────┼─────┼─────┼───────┤
 * │       │ CAT │     │ Dfm │  [  │  ]  │  <- │     │     │  7  │  8  │  9  │  +  │  -  │       │
 * ├───────┼─────┼─────┼─────┼─────┼─────┤     │     │     ├─────┼─────┼─────┼─────┼─────┼───────┤
 * │       │     │     │     │  {  │  }  ├─────┤     ├─────┤  4  │  5  │  6  │  *  │  /  │       │
 * ├───────┼─────┼─────┼─────┼─────┼─────┤     │     │     ├─────┼─────┼─────┼─────┼─────┼───────┤
 * │       │     │     │     │  (  │  )  │     │     │     │  1  │  2  │  3  │  ,  │ Up  │       │
 * └─┬─────┼─────┼─────┼─────┼─────┼─────┴─────┘     └─────┴─────┼─────┼─────┼─────┼─────┼─────┬─┘
 *   │     │     │     │     │     │                             │  0  │  .  │ Lft │ Dwn │ Rgt │
 *   └─────┴─────┴─────┴─────┴─────┘ ┌─────┬─────┐ ┌─────┬─────┐ └─────┴─────┴─────┴─────┴─────┘
 *                                   │ Lft │ Rgt │ │ CLf │ CRt │
 *                             ┌─────┼─────┼─────┤ ├─────┼─────┼─────┐
 *                             │     │     │ SHm │ │ PUp │     │     │
 *                             │ Ent │ Bsp ├─────┤ ├─────┤ Del │ Spc │
 *                             │     │     │ SDn │ │ PDn │     │     │
 *                             └─────┴─────┴─────┘ └─────┴─────┴─────┘
 */
 */
 /* Keymap 2: Numpad Layer
 *
 * ,--------------------------------------------------.           ,--------------------------------------------------.
 * |Version |  F1  |  F2  |  F3  |  F4  |  F5  |  F6  |           |  F7  |  F8  |  F9  |  F10 |  F11 |  F12 |   +    |
 * |--------+------+------+------+------+-------------|           |------+------+------+------+------+------+--------|
 * |        |   !  |   @  |   {  |   }  |   |  |      |           |      |   7  |   8  |   9  |  {[  |  ]}  |   -    |
 * |--------+------+------+------+------+------|      |           |      |------+------+------+------+------+--------|
 * |        |   #  |   $  |   (  |   )  |   `  |------|           |------|   4  |   5  |   6  |  (   |   )  |   *    |
 * |--------+------+------+------+------+------|      |           |      |------+------+------+------+------+--------|
 * |        |   %  |   ^  |   [  |   ]  |   ~  |      |           |      |   1  |   2  |   3  |   ,  |  Up  |   /    |
 * `--------+------+------+------+------+-------------'           `-------------+------+------+------+------+--------'
 *   | EPRM |      |      |      |      |                                       |   0  |   .  | Left | Down | Right |
 *   `----------------------------------'                                       `----------------------------------'
 *                                        ,-------------.       ,-------------.
 *                                        | Home | End  |       | Left | Right|
 *                                 ,------|------|------|       |------+--------+------.
 *                                 |      |      | PgUp |       |  Up  |        |      |
 *                                 | Space|Backsp|------|       |------|  Del   |Enter |
 *                                 |      |ace   | PgDn |       | Down |        |      |
 *                                 `--------------------'       `----------------------'
 */
 /* Keymap 3: Linux Key layer
 *
 * ,--------------------------------------------------.           ,--------------------------------------------------.
 * |  Esc   |   1  |   2  |   3  |   4  |   5  | TgLk |           |   6  |   7  |   8  |   9  |   0  |   -  |   +    |
 * |--------+------+------+------+------+-------------|           |------+------+------+------+------+------+--------|
 * |  Tab   |   Q  |   W  |   E  |   R  |   T  |      |           |      |   Y  |   U  |   I  |   O  |   P  |   \    |
 * |--------+------+------+------+------+------|  =   |           |  <-  |------+------+------+------+------+--------|
 * |   ~    |   A  |   S  |   D  |   F  |   G  |------|           |------|   H  |   J  |   K  |   L  |; / L2|   '    |
 * |--------+------+------+------+------+------|      |           |CtrlF5|------+------+------+------+------+--------|
 * | LShift |   Z  |   X  |   C  |   V  |   B  |      |           |      |   N  |   M  |   ,  |   .  |   /  | RShift |
 * `--------+------+------+------+------+-------------'           `-------------+------+------+------+------+--------'
 *   |LCtrl |CtlAlt|Wn/Cmd| App |  LAlt |                                       | RAlt | RCtl |  [   |  ]   | TgPT |
 *   `----------------------------------'                                      `----------------------------------'
 *                                        ,-------------.       ,-------------.
 *                                        | Home | End  |       | Left | Right|
 *                                 ,------|------|------|       |------+--------+------.
 *                                 |      |      | PgUp |       |  Up  |        |      |
 *                                 | Space|Backsp|------|       |------|  Del   |Enter |
 *                                 |      |ace   | PgDn |       | Down |        |      |
 *                                 `--------------------'       `----------------------'
 */
 
 ```
