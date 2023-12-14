#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=starship
PKG_VERSION:=1.16.0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/starship/starship/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=133888e190ce1563927e16ee693da3026d2e668d975ac373f853e030743775c5

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=ISC
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/starship
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Minimal, blazing-fast, and infinitely customizable prompt for any shell
  DEPENDS:=$(RUST_ARCH_DEPENDS)
  URL:=https://github.com/starship/starship
endef

define Package/starship/description
 The minimal, blazing-fast, and infinitely customizable prompt for any shell.
endef

$(eval $(call RustBinPackage,starship))
$(eval $(call BuildPackage,starship))
