#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=nzbget
PKG_VERSION:=21.1
PKG_RELEASE:=$(AUTORELEASE)

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/nzbget/$(PKG_NAME)/archive/refs/tags/v$(PKG_VERSION)
PKG_HASH:=79695ea503447f13911a9fe58d0ef3e860b2ff5d6fdfd351186ee5fda1ae8bdb

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=GPL-2.0-or-later
PKG_LICENSE_FILES:=COPYING

PKG_INSTALL:=1
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

CONFIGURE_ARGS += \
	--with-libxml2-includes=$(STAGING_DIR)/usr/include/libxml2 \
	--with-libxml2-libraries=$(STAGING_DIR)/usr/lib \
	--with-libcurses-includes=$(STAGING_DIR)/usr/include \
	--with-libcurses-libraries=$(STAGING_DIR)/usr/lib \
	--with-tlslib=OpenSSL \
	--with-openssl-includes=$(STAGING_DIR)/usr/include \
	--with-openssl-libraries=$(STAGING_DIR)/usr/lib \
	--with-zlib-includes=$(STAGING_DIR)/usr/include \
	--with-zlib-libraries=$(STAGING_DIR)/usr/lib

define Package/nzbget
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Binary downloader, which downloads files from Usenet based on information given in nzb-files
  DEPENDS:=+libstdcpp +libncurses +libxml2 +zlib +libopenssl
  URL:=https://github.com/nzbget/nzbget
endef

define Package/nzbget/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/nzbget $(1)/usr/bin/
	$(INSTALL_DIR) $(1)/usr/share/nzbget
	$(CP) $(PKG_INSTALL_DIR)/usr/share/nzbget $(1)/usr/share/

	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) ./files/nzbget.init $(1)/etc/init.d/nzbget
endef

define Package/nzbget/description
 NZBGet is a binary downloader, which downloads files from Usenet based on information given in nzb-files.
endef

$(eval $(call BuildPackage,nzbget))
