PKG_NAME = libgpg-error
PKG_VERS = 1.19
PKG_EXT = tar.bz2
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = ftp://ftp.gnupg.org/gcrypt/$(PKG_NAME)
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS =

HOMEPAGE = http://www.gnupg.org/related_software/libgpg-error/
COMMENT  = Libgpg-error is a small library that defines common error values for all GnuPG components
LICENSE  = LGPL

PRE_CONFIGURE_TARGET = preConfigureTarget
GNU_CONFIGURE = 1

include ../../mk/spksrc.cross-cc.mk

.PHONY: preConfigureTarget
preConfigureTarget:
	cp $(WORK_DIR)/$(PKG_DIR)/src/syscfg/lock-obj-pub.arm-unknown-linux-gnueabi.h $(WORK_DIR)/$(PKG_DIR)/src/syscfg/lock-obj-pub.linux-gnueabi.h
	cp $(WORK_DIR)/$(PKG_DIR)/src/syscfg/lock-obj-pub.x86_64-pc-linux-gnu.h $(WORK_DIR)/$(PKG_DIR)/src/syscfg/lock-obj-pub.linux-gnu.h

