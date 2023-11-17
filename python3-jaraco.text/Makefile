#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-jaraco.text
PKG_VERSION:=3.11.1
PKG_RELEASE:=1

PYPI_NAME:=jaraco.text
PKG_HASH:=333a5df2148f7139718607cdf352fe1d95162971a7299c380dcc24dab0168980

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-jaraco.text
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Module for text manipulation
  URL:=https://github.com/jaraco/jaraco.text
  DEPENDS:= \
    +python3-light
endef

define Package/python3-jaraco.text/description
 This package provides handy routines for dealing with text, such as wrapping, substitution,
 trimming, stripping, prefix and suffix removal, line continuation, indentation, comment processing,
 identifier processing, values parsing, case insensitive comparison, and more.
endef

$(eval $(call Py3Package,python3-jaraco.text))
$(eval $(call BuildPackage,python3-jaraco.text))
$(eval $(call BuildPackage,python3-jaraco.text-src))
