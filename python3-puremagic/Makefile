#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-puremagic
PKG_VERSION:=1.23
PKG_RELEASE:=1

PYPI_NAME:=puremagic
PKG_HASH:=e0bb7dc814b9d606225b57d4d49175d27c24fb745de1a7b3506067f2be54438f

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-puremagic
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Pure python implementation of magic file detection
  URL:=https://github.com/cdgriffith/puremagic
  DEPENDS:= \
    +python3-light
endef

define Package/python3-/description
 puremagic is a pure python module that will identify a file based off it's magic numbers.
endef

$(eval $(call Py3Package,python3-puremagic))
$(eval $(call BuildPackage,python3-puremagic))
$(eval $(call BuildPackage,python3-puremagic-src))
