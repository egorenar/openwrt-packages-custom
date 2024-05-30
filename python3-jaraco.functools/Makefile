#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-jaraco.functools
PKG_VERSION:=4.0.1
PKG_RELEASE:=1

PYPI_NAME:=jaraco.functools
PYPI_SOURCE_NAME=jaraco_functools
PKG_HASH:=d33fa765374c0611b52f8b3a795f8900869aa88c84769d4d1746cd68fb28c3e8

PKG_BUILD_DEPENDS:=python-setuptools-scm/host

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

PYTHON3_PKG_WHEEL_NAME:=jaraco.functools

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
