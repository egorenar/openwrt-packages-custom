#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=bat
PKG_VERSION:=0.24.0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/sharkdp/bat/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=907554a9eff239f256ee8fe05a922aad84febe4fe10a499def72a4557e9eedfb

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE-MIT

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/bat
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=A cat(1) clone with syntax highlighting and Git integration
  DEPENDS:=$(RUST_ARCH_DEPENDS) +zlib
  URL:=https://github.com/sharkdp/bat
endef

define Package/bat/description
 A cat(1) clone with syntax highlighting and Git integration.
endef

$(eval $(call RustBinPackage,bat))
$(eval $(call BuildPackage,bat))
