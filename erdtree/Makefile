#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=erdtree
PKG_VERSION:=3.1.2
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/solidiquis/erdtree/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=1758e7ad8f7be59bc3c6bda8b058097509f9db6f40ad57c4b0b361e3be439297

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/erdtree
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Modern, cross-platform, multi-threaded, and general purpose filesystem and disk-usage utility
  DEPENDS:=$(RUST_ARCH_DEPENDS)
  URL:=https://github.com/solidiquis/erdtree
endef

define Package/erdtree/description
 erdtree is a modern, cross-platform, multi-threaded, and general purpose filesystem and disk-usage
 utility that is aware of .gitignore and hidden file rules.
endef

$(eval $(call RustBinPackage,erdtree))
$(eval $(call BuildPackage,erdtree))
