#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-urwid-mitmproxy
PKG_VERSION:=2.1.2.1
PKG_RELEASE:=1

PYPI_NAME:=urwid-mitmproxy
PKG_HASH:=be6238e587acb92bdd43b241af0a10dc23798e8cf3eddef834164eb637686cda

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=LGPL-2.1-or-later
PKG_LICENSE_FILES:=COPYING

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-urwid-mitmproxy
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=A full-featured console (xterm et al.) user interface library
  URL:=https://github.com/mitmproxy/urwid-mitmproxy
  DEPENDS:= \
    +python3-light
endef

define Package/python3-urwid-mitmproxy/description
 This is an urwid fork with specific patches for mitmproxy.
endef

$(eval $(call Py3Package,python3-urwid-mitmproxy))
$(eval $(call BuildPackage,python3-urwid-mitmproxy))
$(eval $(call BuildPackage,python3-urwid-mitmproxy-src))
