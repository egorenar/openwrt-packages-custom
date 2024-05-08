#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=fd
PKG_VERSION:=10.1.0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/sharkdp/fd/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=ee4b2403388344ff60125c79ff25b7895a170e7960f243ba2b5d51d2c3712d97

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE-MIT

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/fd
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=A simple, fast and user-friendly alternative to find
  DEPENDS:=$(RUST_ARCH_DEPENDS)
  URL:=https://github.com/sharkdp/fd
endef

define Package/fd/description
 A simple, fast and user-friendly alternative to find.
endef

$(eval $(call RustBinPackage,fd))
$(eval $(call BuildPackage,fd))
