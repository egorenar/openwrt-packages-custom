#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-tempora
PKG_VERSION:=5.5.1
PKG_RELEASE:=1

PYPI_NAME:=tempora
PKG_HASH:=a2bb51e2121976d931347b3e433917c364b83fdd5f64ef27336c865bf1fb0f75

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
