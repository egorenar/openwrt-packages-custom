#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-jaraco.functools
PKG_VERSION:=4.0.0
PKG_RELEASE:=1

PYPI_NAME:=jaraco.functools
PKG_HASH:=c279cb24c93d694ef7270f970d499cab4d3813f4e08273f95398651a634f0925

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-jaraco.functools
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Functools like those found in stdlib
  URL:=https://github.com/jaraco/jaraco.functools
  DEPENDS:= \
    +python3-light
endef

define Package/python3-jaraco.functools/description
 Additional functools in the spirit of stdlib's functools.
endef

$(eval $(call Py3Package,python3-jaraco.functools))
$(eval $(call BuildPackage,python3-jaraco.functools))
$(eval $(call BuildPackage,python3-jaraco.functools-src))
