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

.PHONY: help


install: xsession-install config-install
.PHONY: install

xsession-install:
	sudo install -Dm644 ./xsessions/sowm-session.desktop /usr/share/xsessions/sowm-session.desktop
	sudo install -Dm755 ./xsessions/sowm-session /usr/share/sowm/xsessions/sowm-session
.PHONY: xsession-install

config-install:
	sudo install -Dm644 ./config/sowm/environment /usr/share/sowm/config/sowm/environment
	sudo install -Dm755 ./config/sowm/autostart /usr/share/sowm/config/sowm/autostart
.PHONY: config-install




remove: xsession-remove config-remove
.PHONY: remove

xsession-remove:
	sudo rm -f /usr/share/xsessions/sowm-session.desktop
	sudo rm -f /usr/share/sowm/xsessions/sowm-session
.PHONY: xsession-remove

config-remove:
	sudo rm -f /usr/share/sowm/config/sowm/environment
	sudo rm -f /usr/share/sowm/config/sowm/autostart
.PHONY: config-remove
