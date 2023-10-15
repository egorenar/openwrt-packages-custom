#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-rangehttpserver
PKG_VERSION:=1.3.3
PKG_RELEASE:=1

PYPI_NAME:=rangehttpserver
PKG_HASH:=8df6bba60d688f4f349c85ae151cb9e7b83da2c9fd08cf62a3d64ef32e063703

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-rangehttpserver
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=SimpleHTTPServer with support for Range requests
  URL:=https://github.com/danvk/RangeHTTPServer/
  DEPENDS:= \
    +python3-light
endef

define Package/python3-rangehttpserver/description
  SimpleHTTPServer with support for Range requests.
endef

$(eval $(call Py3Package,python3-rangehttpserver))
$(eval $(call BuildPackage,python3-rangehttpserver))
$(eval $(call BuildPackage,python3-rangehttpserver-src))
