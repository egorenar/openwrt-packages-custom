#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-ujson
PKG_VERSION:=5.8.0
PKG_RELEASE:=1

PYPI_NAME:=ujson
PKG_HASH:=78e318def4ade898a461b3d92a79f9441e7e0e4d2ad5419abed4336d702c7425

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-2-Clause
PKG_LICENSE_FILES:=LICENSE.txt

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-ujson
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Ultra fast JSON encoder and decoder for Python
  URL:=https://github.com/ultrajson/ultrajson
  DEPENDS:= \
    +python3-light \
    +libstdcpp
endef

define Package/python3-ujson/description
 UltraJSON is an ultra fast JSON encoder and decoder written in pure C with bindings for Python 3.8+.
endef

$(eval $(call Py3Package,python3-ujson))
$(eval $(call BuildPackage,python3-ujson))
$(eval $(call BuildPackage,python3-ujson-src))
