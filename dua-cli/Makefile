#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=dua-cli
PKG_VERSION:=2.29.2
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/Byron/dua-cli/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=76ebd07c4a4379ef0d45232fa7a9b0bcbff1bd54fad6930ec1a2823806473f5d

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE-MIT

PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/rust/rust-package.mk

define Package/dua-cli
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Tool to conveniently learn about the usage of disk space
  DEPENDS:=$(RUST_ARCH_DEPENDS)
  URL:=Byron/dua-cli
endef

define Package/dua-cli/description
 dua (Disk Usage Analyzer) is a tool to conveniently learn about the usage of disk space of a given directory.
endef

$(eval $(call RustBinPackage,dua-cli))
$(eval $(call BuildPackage,dua-cli))
