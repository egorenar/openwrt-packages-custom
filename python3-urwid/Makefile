#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-urwid
PKG_VERSION:=2.6.15
PKG_RELEASE:=1

PYPI_NAME:=urwid
PKG_HASH:=9ecc57330d88c8d9663ffd7092a681674c03ff794b6330ccfef479af7aa9671b

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=LGPL-2.1-or-later
PKG_LICENSE_FILES:=COPYING

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-urwid
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=A console user interface library for Python
  URL:=https://github.com/urwid/urwid
  DEPENDS:= \
    +python3-light \
    +python3-typing-extensions \
    +python3-wcwidth
endef

define Package/python3-urwid/description
 Urwid is a console user interface library for Python on Linux, OSX, Cygwin or other unix-like OS and partially supports Windows OS (see below).
endef

$(eval $(call Py3Package,python3-urwid))
$(eval $(call BuildPackage,python3-urwid))
$(eval $(call BuildPackage,python3-urwid-src))
