#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=nnn
PKG_VERSION:=4.9
PKG_RELEASE:=$(AUTORELEASE)

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/jarun/$(PKG_NAME)/releases/download/$(PKG_NAME)-$(PKG_VERSION)/
PKG_HASH:=9e25465a856d3ba626d6163046669c0d4010d520f2fb848b0d611e1ec6af1b22

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-2-Clause
PKG_LICENSE_FILES:=LICENSE

PKG_INSTALL:=1
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/nnn
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Full-featured terminal file manager
  DEPENDS:=
  URL:=https://github.com/jarun/nnn
endef

define Package/nn/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/nnn $(1)/usr/bin/
endef

define Package/nnn/description
 nnn is a full-featured terminal file manager. It is tiny, nearly 0-config and incredibly fast.
endef

$(eval $(call BuildPackage,nnn))
