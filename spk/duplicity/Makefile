SPK_NAME = duplicity
SPK_VERS = 0.7.03
SPK_REV = 1
SPK_ICON = src/duplicity.png
DSM_UI_DIR = app

BUILD_DEPENDS = cross/python cross/setuptools cross/pip cross/wheel cross/$(SPK_NAME)
WHEELS = src/requirements.txt
SPK_DEPENDS = "python>=2.7"

MAINTAINER = SynoCommunity
DESCRIPTION = Encrypted bandwidth-efficient backup using the rsync algorithm.
RELOAD_UI = yes
STARTABLE = no
DISPLAY_NAME = Duplicity
CHANGELOG = ""
BETA = 1

HOMEPAGE = http://duplicity.nongnu.org/
LICENSE  = GNU GPL v2

INSTALLER_SCRIPT = src/installer.sh
SSS_SCRIPT       = src/dsm-control.sh

INSTALL_PREFIX = /usr/local/$(SPK_NAME)

COPY_TARGET = nop
POST_STRIP_TARGET = duplicity_extra_install

include ../../mk/spksrc.spk.mk

.PHONY: duplicity_extra_install
duplicity_extra_install:
	install -m 755 -d $(STAGING_DIR)/app
	install -m 755 -d $(STAGING_DIR)/app/images
	install -m 755 -d $(STAGING_DIR)/share
	install -m 755 -d $(STAGING_DIR)/share/wheelhouse
	install -m 644 $(WORK_DIR)/wheelhouse/* $(STAGING_DIR)/share/wheelhouse/
	for size in 16 24 32 48 72 ; \
	do \
	    convert $(SPK_ICON) -thumbnail $${size}x$${size} \
	            $(STAGING_DIR)/app/images/$(SPK_NAME)-$${size}.png ; \
	done
