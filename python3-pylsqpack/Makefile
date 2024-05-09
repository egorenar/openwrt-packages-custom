#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-pylsqpack
PKG_VERSION:=0.3.18
PKG_RELEASE:=1

PYPI_NAME:=pylsqpack
PKG_HASH:=45ae55e721877505f4d5ccd49591d69353f2a548a8673dfafb251d385b3c097f

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-pylsqpack
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Python wrapper for the ls-qpack QPACK library
  URL:=https://github.com/aiortc/pylsqpack
  DEPENDS:= \
    +python3-light
endef

define Package/python3-pylsqpack/description
 pylsqpack is a wrapper around the ls-qpack library. It provides Python Decoder and Encoder
 objects to read or write HTTP/3 headers compressed with QPACK.
endef

$(eval $(call Py3Package,python3-pylsqpack))
$(eval $(call BuildPackage,python3-pylsqpack))
$(eval $(call BuildPackage,python3-pylsqpack-src))
