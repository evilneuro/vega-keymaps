> Originally published on [World of Spectrum](http://live.worldofspectrum.org/vega_plus_keymapping.txt)

## Vega+ V2 key mapping.

What is supposed to happen is the unit reads `zxk` files for games and generates a file on the SD card called `games_data.txt` - this is then read by the unit to list titles you have on the SD card.

However, it seems that the wrong file is created rendering the list unreadable by the unit.

To get round this, you can create the `games_data.txt` file manually.

The contents of the file are exactly the same as the `zxk` file would have been (you don't need to add these now).

For example, to list two titles:-

```
T:Alien 8
F:alien8.z80
M:48
K:;Q;A;O;P;H;1;2;S;3;4;5
D:;UP;DOWN;LEFT;RIGHT;HOLD;1;S;2;A;B;C
T:Atic Atac
F:AticAtac.z80
M:48
K:;Q;A;O;P;H;1;2;S;3;4;5
D:;UP;DOWN;LEFT;RIGHT;HOLD;1;S;2;A;B;C
```

So, to break down what's here:

* `T: Alien 8` - this is the title of the game shown on the list - a bug on pressing the info button means it will always display the first title in the list - that makes no difference.
* `F:` This is the filename you are wanting to play
* `M:` This is the machine type. I believe only 48 or 128 work.
* `K:` This is for the keys (its actually the Vega+ buttons. These are in a specific order, comma separated.

The first entry is unique - it is the sequence of buttons to press to start the game. Some games have more than one button to press to start - so they are separated by a space. So, entering `S 1` here tells the unit to send keypresses `S` & `1` to the title.

Next is the D-Pad directions. The order there is Up, down, left, right - in our example we have mapped them to `Q`, `A`, `O` & `P`.  

Then it's the other buttons - `F`, `1`, `2`, `S` - here we have set `H`, `1`, `2`, `s`

Finally its the bottom 3 buttons.

Any unused or unmapped keys can be left blank, but you still need the comma. In our example, we have no start sequence as you can press `S` to start the games, so the mapped key `s` works.

Finally, we have the `D:` row - this is to display the key meanings when you press the `i` button.

Then rest for other games (the ultimate ones mostly used the same keys so a copy & paste works.

Some keys have special characters:- `EN` (enter), `SP` (space), `CS` (caps shift), `SS` (symbol shift)
