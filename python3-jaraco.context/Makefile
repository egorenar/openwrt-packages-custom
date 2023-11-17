#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-jaraco.context
PKG_VERSION:=4.3.0
PKG_RELEASE:=1

PYPI_NAME:=jaraco.context
PKG_HASH:=4dad2404540b936a20acedec53355bdaea223acb88fd329fa6de9261c941566e

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-jaraco.context
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Context managers by jaraco
  URL:=https://github.com/jaraco/jaraco.context
  DEPENDS:= \
    +python3-light
endef

define Package/python3-jaraco.context/description
 Context managers by jaraco.
endef

$(eval $(call Py3Package,python3-jaraco.context))
$(eval $(call BuildPackage,python3-jaraco.context))
$(eval $(call BuildPackage,python3-jaraco.context-src))
