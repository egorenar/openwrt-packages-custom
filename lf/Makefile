#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=lf
PKG_VERSION:=r32
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/gokcehan/$(PKG_NAME)/archive/$(PKG_VERSION)
PKG_HASH:=01531e7a78d8bfbe14739072e93446d003f0e4ce12032a26671fa326b73bc911

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=golang/host
PKG_BUILD_PARALLEL:=1
PKG_USE_MIPS16:=0

GO_PKG:=github.com/gokcehan/lf

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/feeds/packages/lang/golang/golang-package.mk

define Package/lf
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=A terminal file manager written in Go
  URL:=https://github.com/gokcehan/lf
  DEPENDS:=$(GO_ARCH_DEPENDS)
endef

define Package/lf/description
  A terminal file manager written in Go.
endef

define Package/lf/install
	$(call GoPackage/Package/Install/Bin,$(1))
endef

$(eval $(call GoBinPackage,lf))
$(eval $(call BuildPackage,lf))
