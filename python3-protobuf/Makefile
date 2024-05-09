#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-protobuf
PKG_VERSION:=5.26.1
PKG_RELEASE:=1

PYPI_NAME:=protobuf
PKG_HASH:=8ca2a1d97c290ec7b16e4e5dff2e5ae150cc1582f55b5ab300d45cb0dfa90e51

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-protobuf
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Protocol buffers in Python
  URL:=https://protobuf.dev/
  DEPENDS:= \
    +python3-light \
    +protobuf
endef

define Package/python3-protobuf/description
 Protocol Buffers are language-neutral, platform-neutral extensible mechanisms for serializing structured data.
endef

$(eval $(call Py3Package,python3-protobuf))
$(eval $(call BuildPackage,python3-protobuf))
$(eval $(call BuildPackage,python3-protobuf-src))
