#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=starship
PKG_VERSION:=1.20.1
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/starship/starship/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=851d84be69f9171f10890e3b58b8c5ec6057dd873dc83bfe0bdf965f9844b5dc

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
