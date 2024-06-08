#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=gitui
PKG_VERSION:=0.26.3
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/extrawurst/gitui/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=8075e180f3b01ff0c290b690488a7628c44b4de12346e04a77d823914a48918b

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE.md

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/gitui
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Terminal git GUI
  DEPENDS:=$(RUST_ARCH_DEPENDS)
  URL:=extrawurst/gitui
endef

define Package/gitui/description
 GitUI provides you with the comfort of a git GUI but right in your terminal.
endef

define Build/Compile
	$(call Build/Compile/Cargo,.,--locked)
endef

$(eval $(call RustBinPackage,gitui))
$(eval $(call BuildPackage,gitui))
