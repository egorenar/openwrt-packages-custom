#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=fd
PKG_VERSION:=9.0.0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/sharkdp/fd/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=306d7662994e06e23d25587246fa3fb1f528579e42a84f5128e75feec635a370

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE-MIT

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/fd
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=A simple, fast and user-friendly alternative to find
  DEPENDS:=$(RUST_ARCH_DEPENDS)
  URL:=https://github.com/sharkdp/fd
endef

define Package/fd/description
 A simple, fast and user-friendly alternative to find.
endef

$(eval $(call RustBinPackage,fd))
$(eval $(call BuildPackage,fd))
