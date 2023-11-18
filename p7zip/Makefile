#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=p7zip
PKG_VERSION:=17.05
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/p7zip-project/$(PKG_NAME)/archive/refs/tags/v$(PKG_VERSION)
PKG_HASH:=d2788f892571058c08d27095c22154579dfefb807ebe357d145ab2ddddefb1a6

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=LGPL-2.1-or-later
PKG_LICENSE_FILES:=DOC/License.txt

include $(INCLUDE_DIR)/package.mk

define Package/p7zip
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=File archiver with highest compression ratio
  DEPENDS:=+libstdcpp
  URL:=https://github.com/p7zip-project/p7zip
endef

MAKE_FLAGS += 7z 7za 7zr

define Package/p7zip/install
	$(INSTALL_DIR) $(1)/usr/lib/p7zip
	$(CP) -R $(PKG_BUILD_DIR)/bin/* $(1)/usr/lib/p7zip/

	$(INSTALL_DIR) $(1)/usr/bin/
	$(INSTALL_BIN) ./files/7z $(1)/usr/bin
	$(INSTALL_BIN) ./files/7za $(1)/usr/bin
	$(INSTALL_BIN) ./files/7zr $(1)/usr/bin
endef

define Package/p7zip/description
 p7zip is a quick port of 7z.exe and 7za.exe for Unix. 7-Zip is a file archiver with highest compression ratio.
endef

$(eval $(call BuildPackage,p7zip))
