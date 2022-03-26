#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-charset-normalizer
PKG_VERSION:=2.0.12
PKG_RELEASE:=1

PYPI_NAME:=charset-normalizer
PKG_HASH:=2857e29ff0d34db842cd7ca3230549d1a697f96ee6d3fb071cfa6c7393832597

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=Unlicense
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-charset-normalizer
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Encoding and language detection
  URL:=https://github.com/ousret/charset_normalizer
  DEPENDS:= \
    +python3
endef

define Package/python3-charset-normalizer/description
  A library that helps you read text from an unknown charset encoding.
endef

$(eval $(call Py3Package,python3-charset-normalizer))
$(eval $(call BuildPackage,python3-charset-normalizer))
$(eval $(call BuildPackage,python3-charset-normalizer-src))
