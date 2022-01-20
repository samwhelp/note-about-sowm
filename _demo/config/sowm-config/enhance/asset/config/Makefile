default: help
.PHONY: default

help:
	@echo 'Usage:'
	@echo '	$$ make [action]'
	@echo
	@echo 'Example:'
	@echo '	$$ make'
	@echo '	$$ make help'
	@echo
	@echo '	$$ make install'
	@echo
	@echo '	$$ make remove'
	@echo
	@echo '	$$ make test'
	@echo

.PHONY: help


install: autostart-install config-install compositor-install panel-install wallpaper-install
#	tree --dirsfirst ~/.config/sowm
.PHONY: install

autostart-install:
	install -Dm644 ./sowm/environment ~/.config/sowm/environment
	install -Dm755 ./sowm/autostart ~/.config/sowm/autostart
.PHONY: autostart-install

config-install:
	install -Dm644 ./sowm/sxhkdrc ~/.config/sowm/sxhkdrc
.PHONY: config-install

panel-install:
	install -Dm644 ./sowm/style/tint2/tint2rc ~/.config/sowm/style/tint2/tint2rc
.PHONY: panel-install

compositor-install:
	install -Dm644 ./sowm/style/picom/picom.conf ~/.config/sowm/style/picom/picom.conf
.PHONY: compositor-install

wallpaper-install:
	install -Dm755 ./sowm/bin/sowm-wallpaper-ctrl-shuf ~/.config/sowm/bin/sowm-wallpaper-ctrl-shuf
	install -Dm755 ./sowm/bin/sowm-wallpaper-ctrl-default ~/.config/sowm/bin/sowm-wallpaper-ctrl-default
.PHONY: wallpaper-install




remove: autostart-remove config-remove compositor-remove panel-remove wallpaper-remove
#	tree --dirsfirst ~/.config/sowm
.PHONY: remove

autostart-remove:
	rm -f ~/.config/sowm/environment
	rm -f ~/.config/sowm/autostart
.PHONY: autostart-remove

config-remove:
	rm -f ~/.config/sowm/sxhkdrc
.PHONY: config-remove

panel-remove:
	rm -f  ~/.config/sowm/style/tint2/tint2rc
.PHONY: panel-remove

compositor-remove:
	rm -f  ~/.config/sowm/style/picom/picom.conf
.PHONY: compositor-remove

wallpaper-remove:
	rm -f  ~/.config/sowm/bin/sowm-wallpaper-ctrl-shuf
	rm -f  ~/.config/sowm/bin/sowm-wallpaper-ctrl-default
.PHONY: wallpaper-remove


test:
	./xephyr-run-sowm.sh
.PHONY: test

stop:
	killall -9 bash
.PHONY: stop
