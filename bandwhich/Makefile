#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=bandwhich
PKG_VERSION:=0.23.1
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/imsnif/bandwhich/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=aafb96d059cf9734da915dca4f5940c319d2e6b54e2ffb884332e9f5e820e6d7

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE.md

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/bandwhich
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=CLI utility for displaying current network utilization by process, connection and remote IP/hostname
  DEPENDS:=$(RUST_ARCH_DEPENDS)
  URL:=https://github.com/imsnif/bandwhich
endef

define Package/bandwhich/description
 This is a CLI utility for displaying current network utilization by process, connection and remote IP/hostname.
endef

$(eval $(call RustBinPackage,bandwhich))
$(eval $(call BuildPackage,bandwhich))
