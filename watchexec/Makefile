#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=watchexec
PKG_VERSION:=2.1.2
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/watchexec/watchexec/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=500b886038ccd553559fe19914e1a502728cfeb8ee9d81f3db448b05e5a890ec

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/watchexec
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=A simple, standalone tool that watches a path and runs a command whenever it detects modifications
  DEPENDS:=$(RUST_ARCH_DEPENDS)
  URL:=https://github.com/watchexec/watchexec
endef

define Package/watchexec/description
 watchexec is a simple, standalone tool that watches a path and runs a command whenever it detects modifications.
endef

Build/Compile=$(call Build/Compile/Cargo,crates/cli)

$(eval $(call RustBinPackage,watchexec))
$(eval $(call BuildPackage,watchexec))
