SPK_NAME = attic
SPK_VERS = 0.16
SPK_REV = 2

BUILD_DEPENDS = cross/python3 cross/setuptools cross/pip cross/wheel cross/acl cross/$(SPK_NAME)
WHEELS = $(SPK_NAME)==$(SPK_VERS)
SPK_DEPENDS = "python>=3.4"

MAINTAINER = Lars Immisch
DESCRIPTION = Attic is a deduplicating backup program
RELOAD_UI = yes
DISPLAY_NAME = Attic
CHANGELOG = Initial version 0.16

HOMEPAGE = https://attic-backup.org/

INSTALLER_SCRIPT = src/installer.sh

INSTALL_PREFIX = /usr/local/$(SPK_NAME)

COPY_TARGET = nop
include ../../mk/spksrc.spk.mk
