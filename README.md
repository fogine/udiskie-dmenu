# udiskie-dmenu
Lightweight nodejs script which allows to manage removable devices via `dmenu` (`rofi`) like applications.
This script depends on [udiskie](https://github.com/coldfix/udiskie) (a UDisks front-end that allows to manage removeable media).

Installation
-------------------
`npm install -g udiskie-dmenu`

or copy the `udiskie-dmenu` executable somewhere to `$PATH`

Features
-------------------
* mount
* umount

Usage
-------------------

#### rofi

```bash
    > UDISKIE_DMENU_LAUNCHER=rofi udiskie-dmenu -matching regex -dmenu -i -no-custom -multi-select
```

### dmenu

```bash
    > udiskie-dmenu
```
