#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-pyperclip
PKG_VERSION:=1.9.0
PKG_RELEASE:=1

PYPI_NAME:=pyperclip
PKG_HASH:=b7de0142ddc81bfc5c7507eea19da920b92252b548b96186caf94a5e2527d310

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE.txt

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-pyperclip
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=A cross-platform clipboard module for Python
  URL:=https://github.com/asweigart/pyperclip
  DEPENDS:= \
    +python3-light
endef

define Package/python3-pyperclip/description
 Pyperclip is a cross-platform Python module for copy and paste clipboard functions.
endef

$(eval $(call Py3Package,python3-pyperclip))
$(eval $(call BuildPackage,python3-pyperclip))
$(eval $(call BuildPackage,python3-pyperclip-src))
