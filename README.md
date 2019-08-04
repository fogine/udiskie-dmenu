# udiskie-dmenu
Lightweight nodejs script which allows to manage removable devices via `dmenu` (or `rofi`).  

![Preview](https://github.com/fogine/udiskie-dmenu/raw/master/udiskie-dmenu.gif)

Installation
-------------------
`npm install -g udiskie-dmenu`

or copy the `udiskie-dmenu` executable somewhere to `$PATH`

##### Archlinux
[udiskie-dmenu-git](https://aur.archlinux.org/packages/udiskie-dmenu-git) AUR package

Features
-------------------
* mount
* umount
* Supports Luks encrypted devices

Dependencies
-------------------
* [udiskie](https://github.com/coldfix/udiskie) (python `udisks` & `udisks2` front-end)
* [rofi](https://github.com/DaveDavenport/rofi/) OR [dmenu](http://tools.suckless.org/dmenu/)
* `notify-send`

Usage
-------------------

#### rofi

```bash
    > UDISKIE_DMENU_LAUNCHER="rofi" udiskie-dmenu -matching regex -dmenu -i -no-custom -multi-select
```

User defined shortcut `-kb-custom-1` (defaults to `Alt+1`) will detach drive (umount) by e.g. powering down its physical port.  
The following example redefines the custom shortcut to `Shift+Enter`:
> UDISKIE_DMENU_LAUNCHER='rofi -kb-accept-alt "" -kb-custom-1 "Shift+Return"'

You must ensure that the key combination isn't already binded to other operation (in this case `-kb-accept-alt`).

### dmenu

```bash
    > udiskie-dmenu [dmenu-options]
```

### system notifications

To be notified about `mount` & `umount` device status, run `udiskie` as a daemon when system starts (see `man udiskie` for more info)
