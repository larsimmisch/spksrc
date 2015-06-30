SPK_NAME = attic
SPK_VERS = 0.16
SPK_REV = 1
SPK_ICON = src/Backup-icon.png

BUILD_DEPENDS = cross/python3 cross/setuptools cross/pip cross/wheel cross/acl 
BUILD_DEPENDS += cross/$(SPK_NAME)
WHEELS = $(SPK_NAME)==$(SPK_VERS)
# WHEELS = src/requirements.txt
PIP = pip3
SPK_DEPENDS = "python3>=3.4.1-4"

MAINTAINER = Lars Immisch
DESCRIPTION = Attic is a deduplicating backup program
RELOAD_UI = yes
DISPLAY_NAME = Attic
CHANGELOG = Initial version 0.16

# Copied from homeassistant
UNSUPPORTED_ARCHS = powerpc ppc824x

HOMEPAGE = https://attic-backup.org/

INSTALLER_SCRIPT = src/installer.sh
SSS_SCRIPT       = src/dsm-control.sh

INSTALL_PREFIX = /usr/local/$(SPK_NAME)

COPY_TARGET = nop
POST_STRIP_TARGET = attic_extra_install

include ../../mk/spksrc.spk.mk

.PHONY: attic_extra_install
attic_extra_install:
	install -m 755 -d $(STAGING_DIR)/app
	install -m 755 -d $(STAGING_DIR)/app/images
	install -m 755 -d $(STAGING_DIR)/share
	install -m 755 -d $(STAGING_DIR)/share/wheelhouse
	install -m 644 $(WORK_DIR)/wheelhouse/* $(STAGING_DIR)/share/wheelhouse/
	for size in 16 24 32 48 72; do \
		convert $(SPK_ICON) -thumbnail $${size}x$${size} \
			$(STAGING_DIR)/app/images/$(SPK_NAME)-$${size}.png ; \
	done