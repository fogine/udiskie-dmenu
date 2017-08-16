# udiskie-dmenu
Lightweight nodejs script which allows to manage removable devices via `dmenu` (or `rofi`).  

![Preview](https://github.com/fogine/udiskie-dmenu/raw/master/udiskie-dmenu.gif)

Installation
-------------------
`npm install -g udiskie-dmenu`

or copy the `udiskie-dmenu` executable somewhere to `$PATH`

Features
-------------------
* mount
* umount
* Supports Luks encrypted devices

Dependencies
-------------------
* [udiskie](https://github.com/coldfix/udiskie) (python `udisks` & `udisks2` front-end)
* [rofi](https://github.com/DaveDavenport/rofi/) OR [dmenu](http://tools.suckless.org/dmenu/)

Usage
-------------------

#### rofi

```bash
    > UDISKIE_DMENU_LAUNCHER=rofi udiskie-dmenu -matching regex -dmenu -i -no-custom -multi-select
```

### dmenu

```bash
    > udiskie-dmenu [dmenu-options]
```
