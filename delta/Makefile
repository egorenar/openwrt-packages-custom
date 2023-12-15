#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=delta
PKG_VERSION:=0.16.5
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/dandavison/$(PKG_NAME)/archive/refs/tags/$(PKG_VERSION)
PKG_HASH:=00d4740e9da4f543f34a2a0503615f8190d307d1180dfb753b6911aa6940197f

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/delta
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Syntax-highlighting pager
  DEPENDS:=$(RUST_ARCH_DEPENDS) +zlib
  URL:=https://github.com/dandavison/delta
endef

define Package/delta/description
 Syntax-highlighting pager.
endef

$(eval $(call RustBinPackage,delta))
$(eval $(call BuildPackage,delta))
