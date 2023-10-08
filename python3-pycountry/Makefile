#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-pycountry
PKG_VERSION:=22.3.5
PKG_RELEASE:=1

PYPI_NAME:=pycountry
PKG_HASH:=b2163a246c585894d808f18783e19137cb70a0c18fb36748dc01fc6f109c1646

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=Unlicense
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-pycountry
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Provides databases for various ISO standards
  URL:=https://github.com/flyingcircusio/pycountry
  DEPENDS:= \
    +python3-light
endef

define Package/python3-pycountry/description
  ISO country, subdivision, language, currency and script definitions
  and their translations.
endef

$(eval $(call Py3Package,python3-pycountry))
$(eval $(call BuildPackage,python3-pycountry))
$(eval $(call BuildPackage,python3-pycountry-src))
