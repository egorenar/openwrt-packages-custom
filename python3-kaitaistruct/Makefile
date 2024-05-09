#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-kaitaistruct
PKG_VERSION:=0.10
PKG_RELEASE:=1

PYPI_NAME:=kaitaistruct
PKG_HASH:=a044dee29173d6afbacf27bcac39daf89b654dd418cfa009ab82d9178a9ae52a

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-kaitaistruct
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Kaitai Struct API for Python
  URL:=https://kaitai.io/
  DEPENDS:= \
    +python3-light
endef

define Package/python3-kaitaistruct/description
 Kaitai Struct declarative parser generator for binary data: runtime library for Python.
endef

$(eval $(call Py3Package,python3-kaitaistruct))
$(eval $(call BuildPackage,python3-kaitaistruct))
$(eval $(call BuildPackage,python3-kaitaistruct-src))
