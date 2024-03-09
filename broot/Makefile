#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=broot
PKG_VERSION:=1.36.0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/Canop/broot/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=2929d18c2398afa073f170941a45cd8ab4693d272e1c487c95f7e527569cda99

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/broot
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=A better way to navigate directories
  DEPENDS:=$(RUST_ARCH_DEPENDS) +zlib
  URL:=https://github.com/Canop/broot
endef

define Package/broot/description
 A better way to navigate directories.
endef

$(eval $(call RustBinPackage,broot))
$(eval $(call BuildPackage,broot))
