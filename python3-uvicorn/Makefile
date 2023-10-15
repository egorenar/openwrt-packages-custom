#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-uvicorn
PKG_VERSION:=0.23.2
PKG_RELEASE:=1

PYPI_NAME:=uvicorn
PKG_HASH:=4d3cc12d7727ba72b64d12d3cc7743124074c0a69f7b201512fc50c3e3f1569a

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-2-Clause
PKG_LICENSE_FILES:=LICENSE.md

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-uvicorn
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=ASGI web server implementation
  URL:=https://github.com/encode/uvicorn/
  DEPENDS:= \
    +python3-light \
    +python3-wsproto \
    +python3-websockets \
    +python3-a2wsgi
endef

define Package/python3-uvicorn/description
  Uvicorn is an ASGI web server implementation for Python.
endef

$(eval $(call Py3Package,python3-uvicorn))
$(eval $(call BuildPackage,python3-uvicorn))
$(eval $(call BuildPackage,python3-uvicorn-src))
