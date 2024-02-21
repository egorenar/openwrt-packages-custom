#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=zoxide
PKG_VERSION:=0.9.4
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/ajeetdsouza/zoxide/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=ec002bdca37917130ae34e733eb29d4baa03b130c4b11456d630a01a938e0187

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE-MIT

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/zoxide
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Smarter cd command
  DEPENDS:=$(RUST_ARCH_DEPENDS)
  URL:=https://github.com/ajeetdsouza/zoxide
endef

define Package/zoxide/description
 zoxide is a smarter cd command, inspired by z and autojump.
endef

$(eval $(call RustBinPackage,zoxide))
$(eval $(call BuildPackage,zoxide))
