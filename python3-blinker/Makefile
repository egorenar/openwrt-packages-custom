#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-blinker
PKG_VERSION:=1.8.1
PKG_RELEASE:=1

PYPI_NAME:=blinker
PKG_HASH:=da44ec748222dcd0105ef975eed946da197d5bdf8bafb6aa92f5bc89da63fa25

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-blinker
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Fast, simple object-to-object and broadcast signaling
  URL:=https://github.com/pallets-eco/blinker/
  DEPENDS:= \
    +python3-light
endef

define Package/python3-blinker/description
 Blinker provides a fast dispatching system that allows any number of interested parties
 to subscribe to events, or "signals".
endef

$(eval $(call Py3Package,python3-blinker))
$(eval $(call BuildPackage,python3-blinker))
$(eval $(call BuildPackage,python3-blinker-src))
