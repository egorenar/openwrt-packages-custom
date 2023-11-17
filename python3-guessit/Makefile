#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-guessit
PKG_VERSION:=3.7.1
PKG_RELEASE:=1

PYPI_NAME:=guessit
PKG_HASH:=2c18d982ee6db30db5d59557add0324a2b49bf3940a752947510632a2b58a3c1

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=LGPL-3.0-or-later
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-guessit
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Library for guessing information from video filenames
  URL:=https://github.com/guessit-io/guessit
  DEPENDS:= \
    +python3-light
endef

define Package/python3-guessit/description
 GuessIt is a python library that extracts as much information as possible from a video filename.
endef

$(eval $(call Py3Package,python3-guessit))
$(eval $(call BuildPackage,python3-guessit))
$(eval $(call BuildPackage,python3-guessit-src))
