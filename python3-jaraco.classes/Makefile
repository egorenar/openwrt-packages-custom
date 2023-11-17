#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-jaraco.classes
PKG_VERSION:=3.3.0
PKG_RELEASE:=1

PYPI_NAME:=jaraco.classes
PKG_HASH:=c063dd08e89217cee02c8d5e5ec560f2c8ce6cdc2fcdc2e68f7b2e5547ed3621

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-jaraco.classes
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Utility functions for Python class constructs
  URL:=https://github.com/jaraco/jaraco.classes
  DEPENDS:= \
    +python3-light
endef

define Package/python3-jaraco.classes/description
 Utility functions for Python class constructs.
endef

$(eval $(call Py3Package,python3-jaraco.classes))
$(eval $(call BuildPackage,python3-jaraco.classes))
$(eval $(call BuildPackage,python3-jaraco.classes-src))
