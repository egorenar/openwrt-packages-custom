#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=shntool
PKG_VERSION:=3.0.10
PKG_RELEASE:=$(AUTORELEASE)

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=http://shnutils.freeshell.org/shntool/dist/src/
PKG_HASH:=74302eac477ca08fb2b42b9f154cc870593aec8beab308676e4373a5e4ca2102

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=GPL-1.0-or-later
PKG_LICENSE_FILES:=COPYING

PKG_INSTALL:=1
PKG_FIXUP:=autoreconf
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/shntool
  SECTION:=sound
  CATEGORY:=Sound
  TITLE:=Multi-purpose WAVE data processing and reporting utility
  DEPENDS:=+libflac
  URL:=http://shnutils.freeshell.org/shntool/
endef

define Package/shntool/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/shn* $(1)/usr/bin/
endef

define Package/shntool/description
  shntool is a multi-purpose WAVE data processing and reporting utility.
  File formats are abstracted from its core, so it can process any file that
  contains WAVE data, compressed or not - provided there exists a format module
  to handle that particular file type.
endef

$(eval $(call BuildPackage,shntool))
