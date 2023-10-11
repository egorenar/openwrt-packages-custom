#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=mp3unicode
PKG_VERSION:=1.2.1
PKG_RELEASE:=$(AUTORELEASE)

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_SOURCE_URL:=https://github.com/alonbl/$(PKG_NAME)/releases/download/$(PKG_NAME)-$(PKG_VERSION)/
PKG_HASH:=375b432ce784407e74fceb055d115bf83b1bd04a83b95256171e1a36e00cfe07

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=GPL-2.0-or-later
PKG_LICENSE_FILES:=COPYING

PKG_INSTALL:=1
PKG_FIXUP:=autoreconf
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/mp3unicode
  SECTION:=sound
  CATEGORY:=Sound
  TITLE:=Converts ID3 tags in mp3 files between different encodings
  DEPENDS:=+taglib
  URL:=https://github.com/alonbl/mp3unicode
endef

define Package/mp3unicode/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/mp3unicode $(1)/usr/bin/
endef

define Package/mp3unicode/description
  MP3Unicode is a command line utility to convert ID3 tags in mp3 files between
  different encodings.
endef

$(eval $(call BuildPackage,mp3unicode))
