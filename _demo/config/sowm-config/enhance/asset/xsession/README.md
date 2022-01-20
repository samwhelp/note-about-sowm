
# Boot

## Subject

* [Xsession](#xsession)
* [Autostart](#autostart)
* [Howto](#howto)


## Xsession

| Path | Note |
| --- | --- |
| [/usr/share/xsessions/sowm-session.desktop](xsessions/sowm-session.desktop) | start here |
| [/usr/share/sowm/xsessions/sowm-session](xsessions/sowm-session) | sowm-session.desktop call this script |


## Autostart

> Not using system wild if user file exists.

### System Wild

| Path |
| --- |
| [/usr/share/sowm/config/sowm/environment](config/sowm/environment) |
| [/usr/share/sowm/config/sowm/autostart](config/sowm/autostart) |


### Per User

| Path |
| --- |
| [~/.config/sowm/environment](../config/sowm/environment) |
| [~/.config/sowm/autostart](../config/sowm/autostart) |


## Howto

### Install

``` sh
make install
```

### Remove

``` sh
make remove
```
