#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-portend
PKG_VERSION:=3.2.0
PKG_RELEASE:=1

PYPI_NAME:=portend
PKG_HASH:=5250a352c19c959d767cac878b829d93e5dc7625a5143399a2a00dc6628ffb72

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-portend
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=TCP port monitoring and discovery
  URL:=https://github.com/jaraco/portend
  DEPENDS:= \
    +python3-light
endef

define Package/python3-portend/description
 Use portend to monitor TCP ports for bound or unbound states.
endef

$(eval $(call Py3Package,python3-portend))
$(eval $(call BuildPackage,python3-portend))
$(eval $(call BuildPackage,python3-portend-src))
