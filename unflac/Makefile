#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=unflac
PKG_VERSION:=1.1
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://git.sr.ht/~ft/unflac/archive/
PKG_HASH:=a79aa3625bae55286f382909a899f6304d71e7ce206e0234c40d944c74932caf

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=Unlicense
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=golang/host
PKG_BUILD_PARALLEL:=1
PKG_USE_MIPS16:=0

GO_PKG:=git.sr.ht/~ft/unflac

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/feeds/packages/lang/golang/golang-package.mk

define Package/unflac
  SECTION:=sound
  CATEGORY:=Sound
  TITLE:=A command line tool for fast frame accurate audio image + cue sheet splitting
  URL:=https://git.sr.ht/~ft/unflac/
  DEPENDS:=$(GO_ARCH_DEPENDS) +ffmpeg +ffprobe
endef

define Package/unflac/description
  A command line tool for fast frame accurate audio image + cue sheet splitting
endef

define Package/unflac/install
	$(call GoPackage/Package/Install/Bin,$(1))
endef

$(eval $(call GoBinPackage,unflac))
$(eval $(call BuildPackage,unflac))
