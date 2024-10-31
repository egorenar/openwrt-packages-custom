#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=hexyl
PKG_VERSION:=0.15.0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/sharkdp/hexyl/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=017ab7fe18caa3d13427fb13fd6050a9d8bf9aa26d1e1fe02924dfd7f86cd3cf

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE-MIT

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/hexyl
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Simple hex viewer for the terminal
  DEPENDS:=$(RUST_ARCH_DEPENDS)
  URL:=https://github.com/sharkdp/hexyl
endef

define Package/hexyl/description
 hexyl is a simple hex viewer for the terminal.
endef

$(eval $(call RustBinPackage,hexyl))
$(eval $(call BuildPackage,hexyl))
