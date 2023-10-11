#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-soco
PKG_VERSION:=0.29.1
PKG_RELEASE:=1

PYPI_NAME:=soco
PKG_HASH:=6f164ab8c282d5d2e4cc382d55b7e7c1bb45f400d7e784f64b50f97a6c9f7363

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE.rst

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-soco
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=SoCo (Sonos Controller) is a simple library to control Sonos speakers
  URL:=https://github.com/SoCo/SoCo
  DEPENDS:= \
    +python3-light \
    +python3-requests \
    +python3-xmltodict \
    +python3-ifaddr \
    +python3-appdirs \
    +python3-lxml
endef

define Package/python3-soco/description
  SoCo (Sonos Controller) is a simple library to control Sonos speakers.
endef

$(eval $(call Py3Package,python3-soco))
$(eval $(call BuildPackage,python3-soco))
$(eval $(call BuildPackage,python3-soco-src))
