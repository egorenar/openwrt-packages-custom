#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-zstandard
PKG_VERSION:=0.22.0
PKG_RELEASE:=1

PYPI_NAME:=zstandard
PKG_HASH:=8226a33c542bcb54cd6bd0a366067b610b41713b64c9abec1bc4533d69f51e70

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=python-cffi/host python-wheel/host

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-zstandard
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Zstandard bindings for Python
  URL:=https://github.com/indygreg/python-zstandard
  DEPENDS:= \
    +python3-light
endef

define Package/python3-zstandard/description
 This project provides Python bindings for interfacing with the Zstandard compression library.
 A C extension and CFFI interface are provided.
endef

$(eval $(call Py3Package,python3-zstandard))
$(eval $(call BuildPackage,python3-zstandard))
$(eval $(call BuildPackage,python3-zstandard-src))
