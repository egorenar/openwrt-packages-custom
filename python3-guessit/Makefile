#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-guessit
PKG_VERSION:=3.8.0
PKG_RELEASE:=1

PYPI_NAME:=guessit
PKG_HASH:=6619fcbbf9a0510ec8c2c33744c4251cad0507b1d573d05c875de17edc5edbed

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
