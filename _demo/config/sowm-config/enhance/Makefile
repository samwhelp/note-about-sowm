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
	@echo '	$$ make clone'
	@echo
	@echo '	$$ make prepare-arch-build'
	@echo
	@echo '	$$ make build'
	@echo
	@echo '	$$ make install'
	@echo
	@echo '	$$ make remove'
	@echo

.PHONY: help


install: sowm-install xsession-install config-install
.PHONY: install

remove: sowm-remove xsession-remove config-remove
.PHONY: remove


##
## * https://aur.archlinux.org/packages/?K=sowm
## * https://aur.archlinux.org/packages/sowm/
## * https://aur.archlinux.org/cgit/aur.git/tree/PKGBUILD?h=sowm
##

prepare-arch-build:
	sudo pacman -Sy --needed libx11
.PHONY: prepare-arch-build

clone:
	git clone https://github.com/dylanaraps/sowm.git src/sowm
.PHONY: clone

build:
	cp -a asset/overlay/sowm/config.h src/sowm/config.h
	make -C src/sowm
.PHONY: build

sowm-install: build
#	sudo install -Dm755 ./src/sowm/sowm /usr/bin/sowm
	sudo install -Dm755 ./src/sowm/sowm /usr/local/bin/sowm
.PHONY: sowm-install


sowm-remove:
#	sudo rm -f /usr/bin/sowm
	sudo rm -f /usr/local/bin/sowm
.PHONY: sowm-remove




xsession-install:
	make -C ./asset/xsession install
.PHONY: xsession-install

xsession-remove:
	make -C ./asset/xsession remove
.PHONY: xsession-remove




config-install:
	make -C ./asset/config install
.PHONY: config-install

config-remove:
	make -C ./asset/config remove
.PHONY: config-remove
