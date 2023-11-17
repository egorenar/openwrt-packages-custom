#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-sabctools
PKG_VERSION:=7.1.2
PKG_RELEASE:=1

PYPI_NAME:=sabctools
PKG_HASH:=c038055eec5c966a8c9515f2afdaa9aee24970e5df3a23964d95d7e77b98101f

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
