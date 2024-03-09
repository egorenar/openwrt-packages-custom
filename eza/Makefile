#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=eza
PKG_VERSION:=0.18.6
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/eza-community/eza/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=4cbca009d8ddc817d9ffda34bd1cada4278896e63051c645f0821605a6497faa

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/eza
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=A modern, maintained replacement for ls
  DEPENDS:=$(RUST_ARCH_DEPENDS) +zlib
  URL:=https://github.com/eza-community/eza
endef

define Package/eza/description
 A modern, maintained replacement for ls.
endef

$(eval $(call RustBinPackage,eza))
$(eval $(call BuildPackage,eza))
