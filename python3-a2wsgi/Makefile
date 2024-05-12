#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-a2wsgi
PKG_VERSION:=1.8.0
PKG_RELEASE:=1

PYPI_NAME:=a2wsgi
PKG_HASH:=b20436b92f33db9ff1436be64b86e82e187096ebb5d1a52de2794a70db981510

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=
PKG_LICENSE_FILES:=LICENSE.md

HOST_PYTHON3_PACKAGE_BUILD_DEPENDS=./pdm-backend.txt

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-a2wsgi
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Convert WSGI app to ASGI app or ASGI app to WSGI app
  URL:=https://github.com/abersheeran/a2wsgi/
  DEPENDS:= \
    +python3-light \
    +python3-asgiref
endef

define Package/python3-a2wsgi/description
  Convert WSGI app to ASGI app or ASGI app to WSGI app.
endef

$(eval $(call Py3Package,python3-a2wsgi))
$(eval $(call BuildPackage,python3-a2wsgi))
$(eval $(call BuildPackage,python3-a2wsgi-src))
