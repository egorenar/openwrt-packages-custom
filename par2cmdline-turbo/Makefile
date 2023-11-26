#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=par2cmdline-turbo
PKG_VERSION:=1.1.1
PKG_RELEASE:=$(AUTORELEASE)

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/animetosho/$(PKG_NAME)/archive/refs/tags/v$(PKG_VERSION)
PKG_HASH:=df2ed7c0ab4eb70347d2fe6c7ed36a0bd5b4b750e7dbdb842d89c51409c716fc

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=GPL-2.0-or-later
PKG_LICENSE_FILES:=COPYING

PKG_INSTALL:=1
PKG_FIXUP:=autoreconf
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/par2cmdline-turbo
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=PAR 2.0 compatible file verification and repair tool
  DEPENDS:=+libstdcpp +libatomic
  URL:=https://github.com/animetosho/par2cmdline-turbo
endef

define Package/par2cmdline-turbo/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/par2 $(1)/usr/bin/
	$(LN) par2 $(1)/usr/bin/par2create
	$(LN) par2 $(1)/usr/bin/par2verify
	$(LN) par2 $(1)/usr/bin/par2repair
endef

define Package/par2cmdline-turbo/description
 This is a simple fork of par2cmdline which replaces core computation routines with ParPar’s processing backend,
 improving par2cmdline’s performance on x86/ARM platforms.
endef

$(eval $(call BuildPackage,par2cmdline-turbo))
