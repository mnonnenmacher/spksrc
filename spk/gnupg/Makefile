SPK_NAME = gnupg
SPK_VERS = 2.1.6
SPK_REV = 1
SPK_ICON = src/gnupg.png
DSM_UI_DIR = app

DEPENDS = cross/$(SPK_NAME)

MAINTAINER = SynoCommunity
DESCRIPTION = GnuPG allows to encrypt and sign your data and communication, features a versatile key management system as well as access modules for all kinds of public key directories.
RELOAD_UI = yes
STARTABLE = no
DISPLAY_NAME = GnuPG
CHANGELOG = ""
BETA = 1

HOMEPAGE = http://www.gnupg.org/
LICENSE  = GNU General Public License

INSTALLER_SCRIPT = src/installer.sh
SSS_SCRIPT       = src/dsm-control.sh

INSTALL_PREFIX = /usr/local/$(SPK_NAME)

POST_STRIP_TARGET = gnupg_extra_install

include ../../mk/spksrc.spk.mk

.PHONY: gnupg_extra_install
gnupg_extra_install:
	install -m 755 -d $(STAGING_DIR)/app
	install -m 755 -d $(STAGING_DIR)/app/images
	for size in 16 24 32 48 72 ; \
	do \
	    convert $(SPK_ICON) -thumbnail $${size}x$${size} \
	            $(STAGING_DIR)/app/images/$(SPK_NAME)-$${size}.png ; \
	done
