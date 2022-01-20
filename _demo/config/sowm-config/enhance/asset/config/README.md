
# User Config


## Subject

* [User Config Dir Path](#user-config-dir-path)
* [User Config File List](#user-config-file-list)
* [Howto](#howto)


## User Config Dir Path

* [~/.config/sowm](./)

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
├── sxhkdrc
└── sowmrc

4 directories, 8 files
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
