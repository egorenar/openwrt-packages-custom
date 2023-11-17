#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-rebulk
PKG_VERSION:=3.2.0
PKG_RELEASE:=1

PYPI_NAME:=rebulk
PKG_HASH:=0d30bf80fca00fa9c697185ac475daac9bde5f646ce3338c9ff5d5dc1ebdfebc

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-rebulk
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Library for advanced searches in strings
  URL:=https://github.com/Toilal/rebulk/
  DEPENDS:= \
    +python3-light
endef

define Package/python3-rebulk/description
  ReBulk is a python library that performs advanced searches in strings that would be hard
  to implement using re module or String methods only.
endef

$(eval $(call Py3Package,python3-rebulk))
$(eval $(call BuildPackage,python3-rebulk))
$(eval $(call BuildPackage,python3-rebulk-src))
