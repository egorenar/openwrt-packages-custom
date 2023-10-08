#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-trio-websocket
PKG_VERSION:=0.11.1
PKG_RELEASE:=1

PYPI_NAME:=trio-websocket
PKG_HASH:=18c11793647703c158b1f6e62de638acada927344d534e3c7628eedcb746839f

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=Unlicense
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-trio-websocket
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Server and client library for the WebSocket protocol
  URL:=https://github.com/python-trio/trio-websocket/
  DEPENDS:= \
    +python3-light \
    +python3-trio \
    +python3-cryptography \
    +python3-click \
    +python3-wsproto
endef

define Package/python3-trio-websocket/description
  This library implements both server and client aspects of the the WebSocket protocol,
  striving for safety, correctness, and ergonomics. It is based on the wsproto project,
  which is a Sans-IO state machine that implements the majority of the WebSocket protocol,
  including framing, codecs, and events. This library handles I/O using the Trio framework.
endef

$(eval $(call Py3Package,python3-trio-websocket))
$(eval $(call BuildPackage,python3-trio-websocket))
$(eval $(call BuildPackage,python3-trio-websocket-src))
