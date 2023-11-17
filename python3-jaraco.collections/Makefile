#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-jaraco.collections
PKG_VERSION:=4.3.0
PKG_RELEASE:=1

PYPI_NAME:=jaraco.collections
PKG_HASH:=74ffc23fccfee4de0a2ebf556a33675b6a3c003d6335947d3122a0bc8822c8e4

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-jaraco.collections
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Collection objects similar to those in stdlib by jaraco
  URL:=https://github.com/jaraco/jaraco.collections
  DEPENDS:= \
    +python3-light
endef

define Package/python3-jaraco.collections/description
 Models and classes to supplement the stdlib 'collections' module.
endef

$(eval $(call Py3Package,python3-jaraco.collections))
$(eval $(call BuildPackage,python3-jaraco.collections))
$(eval $(call BuildPackage,python3-jaraco.collections-src))
