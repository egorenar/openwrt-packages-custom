#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-wsproto
PKG_VERSION:=1.2.0
PKG_RELEASE:=1

PYPI_NAME:=wsproto
PKG_HASH:=ad565f26ecb92588a3e43bc3d96164de84cd9902482b130d0ddbaa9664a85065

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=Unlicense
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-wsproto
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=WebSockets state-machine based protocol implementation
  URL:=https://github.com/python-hyper/wsproto/
  DEPENDS:= \
    +python3-light
endef

define Package/python3-wsproto/description
  A pure-Python implementation of a WebSocket protocol stack.
endef

$(eval $(call Py3Package,python3-wsproto))
$(eval $(call BuildPackage,python3-wsproto))
$(eval $(call BuildPackage,python3-wsproto-src))
