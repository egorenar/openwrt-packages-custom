#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-pycountry
PKG_VERSION:=23.12.11
PKG_RELEASE:=1

PYPI_NAME:=pycountry
PKG_HASH:=00569d82eaefbc6a490a311bfa84a9c571cff9ddbf8b0a4f4e7b4f868b4ad925

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=LGPL-2.1-or-later
PKG_LICENSE_FILES:=LICENSE.txt

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
