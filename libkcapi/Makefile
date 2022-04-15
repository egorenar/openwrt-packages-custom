#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=libkcapi
PKG_VERSION:=1.4.0
PKG_RELEASE:=$(AUTORELEASE)

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.xz
PKG_SOURCE_URL:=https://www.chronox.de/libkcapi/
PKG_HASH:=644b47593b3f27f08add7a8808ccdbe569a2f331d70fb8b52551e57379b917fa

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-3-Clause (library), BSD-3-Clause or GPL-2.0 (programs)
PKG_LICENSE_FILES:=COPYING COPYING.gplv2 COPYING.bsd

PKG_INSTALL:=1
PKG_FIXUP:=autoreconf
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

CONFIGURE_VARS += \
	LDFLAGS_FOR_BUILD="$(HOST_LDFLAGS)" \
	CPPFLAGS_FOR_BUILD="$(HOST_CPPFLAGS)" \
	CFLAGS_FOR_BUILD="$(HOST_CFLAGS)" \
	CC_FOR_BUILD="$(HOSTCC)" \
	ac_cv_path_DB2PDF="" \
	ac_cv_path_DB2PS="" \
	ac_cv_path_XMLTO=""

CONFIGURE_ARGS += \
	--enable-kcapi-encapp \
	--enable-kcapi-hasher \
	--enable-kcapi-dgstapp \
	--enable-kcapi-rngapp \
	--enable-kcapi-speed \
	--enable-kcapi-test

TARGET_CFLAGS += -Wno-error=sign-conversion

MAKE_FLAGS := \
	CCOPT="$(TARGET_CFLAGS)"

define Package/libkcapi
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=Linux Kernel Crypto API userspace interface library
  DEPENDS:=
  URL:=https://www.chronox.de/libkcapi.html
endef

define Package/libkcapi/description
  Linux Kernel Crypto API userspace interface library
endef

define Build/InstallDev
	$(INSTALL_DIR) $(1)/usr/include
	$(CP) $(PKG_INSTALL_DIR)/usr/include/kcapi.h $(1)/usr/include/

	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libkcapi.so* $(1)/usr/lib/

	$(INSTALL_DIR) $(1)/usr/lib/pkgconfig
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/pkgconfig/libkcapi.pc $(1)/usr/lib/pkgconfig/
endef

define Package/libkcapi/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libkcapi.so* $(1)/usr/lib/

	$(INSTALL_DIR) $(1)/usr/lib/libkcapi
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libkcapi/* $(1)/usr/lib/libkcapi/

	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/kcapi $(1)/usr/bin/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/kcapi-convenience $(1)/usr/bin/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/kcapi-enc $(1)/usr/bin/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/kcapi-enc-test-large $(1)/usr/bin/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/kcapi-dgst $(1)/usr/bin/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/kcapi-rng $(1)/usr/bin/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/kcapi-speed $(1)/usr/bin/
	$(CP) $(PKG_INSTALL_DIR)/usr/bin/s*hmac $(1)/usr/bin/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/fipscheck $(1)/usr/bin/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/fipshmac $(1)/usr/bin/
endef

$(eval $(call BuildPackage,libkcapi))
