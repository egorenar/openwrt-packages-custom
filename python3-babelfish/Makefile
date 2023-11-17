#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-babelfish
PKG_VERSION:=0.6.0
PKG_RELEASE:=1

PYPI_NAME:=babelfish
PKG_HASH:=2dadfadd1b205ca5fa5dc9fa637f5b7933160a0418684c7c46a7a664033208a2

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=python-poetry-core/host

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-babelfish
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=A module to work with countries and languages
  URL:=https://github.com/Diaoul/babelfish
  DEPENDS:= \
    +python3-light
endef

define Package/python3-babelfish/description
 BabelFish is a Python library to work with countries and languages.
endef

$(eval $(call Py3Package,python3-babelfish))
$(eval $(call BuildPackage,python3-babelfish))
$(eval $(call BuildPackage,python3-babelfish-src))
