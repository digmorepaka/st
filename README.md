# digmorepaka's suckful-ST
Based off Luke Smith's fork. 

Changes:
+ Dark background 
+ White foreground
+ Mouse paste
+ TTF Terminus font

## Changes made by Luke Smith:
+ transparency
+ copy to clipboard (alt-shift-c)
+ Optional compatibility with `Xresources` and `pywal` for dynamic colors
+ Solarized colors (light and dark toggleable)
+ vertcenter
+ scrollback with keyboard
+ scrollback with mouse
+ updated to latest version 0.8.1
+ Hold alt and press either ↑/↓ or the vim keys k/j to move up/down in the terminal.
+ Alt-u and Alt-d scroll back/forward in history a page at a time.
+ Alt-PageUp and Alt-PageDown scroll back/forward in history a page at a time.
+ Zoom in/out with Alt+Shift+k/j or u/d for larger intervals.

## Original ST bindings:

+ Scroll through history -- Shift+PageUp/PageDown or Shift+Mouse wheel
+ Increase/decrease font size -- Shift+Alt+PageUp/PageDown
+ Return to default font size -- Shift+Alt+Home
+ Paste -- Shift+Insert

## Installation for newbs

```
make
sudo make install
```

## Dependencies: 
+ `make`
+ `libX11`
+ `libXft`
Some of these might need -dev on distros like Debian.
## Custom changes (`config.def.h` or `config.h`)

### `Xresources` and `pywal`/`wal` compatibility

If you use `wal` to maintain color schemes across your programs, you can use the `xresources.patch`.

```
patch < xresources.patch
make && sudo make install
```

## Explore `config.h`

+ Change `colorname[]` array values (88 LOC), 
+ Numbers of 0 - 15 are usual terminal colors. Change them to your liking.
+ Change `bg` to your desired terminal background color.
+ Change `fg` to your desired terminal foreground color.
+ Change `cursor` to your desired terminal cursor color.
