#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=dysk
PKG_VERSION:=2.8.2
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/Canop/dysk/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=3e0f3a470539721748d7bc1acc867bdddcb824695b2f766e3a1f230ebac28c2c

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/dysk
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=A linux utility listing your filesystems
  DEPENDS:=$(RUST_ARCH_DEPENDS)
  URL:=https://github.com/Canop/dysk
endef

define Package/dysk/description
 A linux utility listing your filesystems.
endef

$(eval $(call RustBinPackage,dysk))
$(eval $(call BuildPackage,dysk))
