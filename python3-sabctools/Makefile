#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-sabctools
PKG_VERSION:=8.1.0
PKG_RELEASE:=1

PYPI_NAME:=sabctools
PKG_HASH:=3d87db991f704f74874fea05c90176175de0ec581dbd8fe5f69d03eb973ff915

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=GPL-2.0-or-later
PKG_LICENSE_FILES:=LICENSE.md

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-sabctools
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=C implementations of functions for use within SABnzbd
  URL:=https://github.com/sabnzbd/sabctools/
  DEPENDS:= \
    +python3-light \
    +libstdcpp
endef

define Package/python3-sabctools/description
 C implementations of functions for use within SABnzbd.
endef

$(eval $(call Py3Package,python3-sabctools))
$(eval $(call BuildPackage,python3-sabctools))
$(eval $(call BuildPackage,python3-sabctools-src))
