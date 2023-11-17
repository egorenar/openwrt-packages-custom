#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=par2cmdline
PKG_VERSION:=0.8.1
PKG_RELEASE:=$(AUTORELEASE)

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_SOURCE_URL:=https://github.com/Parchive/$(PKG_NAME)/releases/download/v$(PKG_VERSION)/
PKG_HASH:=5fcd712cae2b73002b0bf450c939b211b3d1037f9bb9c3ae52d6d24a0ba075e4

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=GPL-2.0-or-later
PKG_LICENSE_FILES:=COPYING

PKG_INSTALL:=1
PKG_FIXUP:=autoreconf
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/par2cmdline
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=PAR 2.0 compatible file verification and repair tool
  DEPENDS:=+libstdcpp
  URL:=https://github.com/Parchive/par2cmdline
endef

define Package/par2cmdline/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/par2 $(1)/usr/bin/
	$(LN) par2 $(1)/usr/bin/par2create
	$(LN) par2 $(1)/usr/bin/par2verify
	$(LN) par2 $(1)/usr/bin/par2repair
endef

define Package/par2cmdline/description
 par2cmdline is a PAR 2.0 compatible file verification and repair tool.
endef

$(eval $(call BuildPackage,par2cmdline))
