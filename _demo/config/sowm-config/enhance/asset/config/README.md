
# Sowm / User Config


## Subject

* [Spec](#spec)
* [User Config Dir Path](#user-config-dir-path)
* [User Config File List](#user-config-file-list)
* [Howto](#howto)
* [Test Command](#test-command)


## Spec

* [Keybind](spec-keybind.md)


## User Config Dir Path

* [~/.config/sowm](./sowm)

## User Config File List

run

``` sh
tree --dirsfirst ~/.config/sowm
```

show

```
/home/user/.config/sowm
├── bin
│   ├── sowm-wallpaper-ctrl-default
│   └── sowm-wallpaper-ctrl-shuf
├── style
│   ├── picom
│   │   └── picom.conf
│   └── tint2
│       └── tint2rc
├── autostart
├── environment
└── sxhkdrc

4 directories, 7 files
```




## Howto

### Install

``` sh
make install
```

### Remove

``` sh
make remove
```

## Test Command

``` sh
xmodmap -pk
```

``` sh
xev -event keyboard
```
