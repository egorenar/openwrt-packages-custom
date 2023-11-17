#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-tempora
PKG_VERSION:=5.5.0
PKG_RELEASE:=1

PYPI_NAME:=tempora
PKG_HASH:=13e4fcc997d0509c3306d6841f03e9381b7e5e46b2bebfae9151af90085f0c26

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-tempora
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Objects and routines pertaining to date and time (tempora)
  URL:=https://github.com/jaraco/tempora
  DEPENDS:= \
    +python3-light
endef

define Package/python3-tempora/description
 Objects and routines pertaining to date and time (tempora).
endef

$(eval $(call Py3Package,python3-tempora))
$(eval $(call BuildPackage,python3-tempora))
$(eval $(call BuildPackage,python3-tempora-src))
