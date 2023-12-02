#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=sd
PKG_VERSION:=1.0.0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/chmln/sd/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=2adc1dec0d2c63cbffa94204b212926f2735a59753494fca72c3cfe4001d472f

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/sd
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=An intuitive find & replace CLI
  DEPENDS:=$(RUST_ARCH_DEPENDS)
  URL:=https://github.com/chmln/sd
endef

define Package/sd/description
 sd is an intuitive find & replace CLI.
endef

$(eval $(call RustBinPackage,sd))
$(eval $(call BuildPackage,sd))
