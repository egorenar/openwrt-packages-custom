#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-isodate
PKG_VERSION:=0.6.1
PKG_RELEASE:=1

PYPI_NAME:=isodate
PKG_HASH:=48c5881de7e8b0a0d648cb024c8062dc84e7b840ed81e864c7614fd3c127bde9

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=Unlicense
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-isodate
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Used for parsing ISO8601 strings
  URL:=https://github.com/gweis/isodate/
  DEPENDS:= \
    +python3 \
    +python3-six
endef

define Package/python3-isodate/description
  This module implements ISO 8601 date, time and duration parsing.
endef

$(eval $(call Py3Package,python3-isodate))
$(eval $(call BuildPackage,python3-isodate))
$(eval $(call BuildPackage,python3-isodate-src))
