#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-h11
PKG_VERSION:=0.14.0
PKG_RELEASE:=1

PYPI_NAME:=h11
PKG_HASH:=8f19fbbe99e72420ff35c00b27a34cb9937e902a8b810e2c88300c6f0a3b699d

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE.txt

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-h11
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=A pure-Python, bring-your-own-I/O implementation of HTTP/1.1
  URL:=https://github.com/python-hyper/h11
  DEPENDS:= \
    +python3-light
endef

define Package/python3-h11/description
 This is a little HTTP/1.1 library written from scratch in Python, heavily inspired by hyper-h2.
endef

$(eval $(call Py3Package,python3-h11))
$(eval $(call BuildPackage,python3-h11))
$(eval $(call BuildPackage,python3-h11-src))
