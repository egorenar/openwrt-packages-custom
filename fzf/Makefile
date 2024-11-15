#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=fzf
PKG_VERSION:=0.56.3
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/junegunn/$(PKG_NAME)/archive/refs/tags/v$(PKG_VERSION)
PKG_HASH:=fc7bf3fcfdc3c9562237d1e82196618201a39b3fd6bf3364149516b288f5a24a

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=golang/host
PKG_BUILD_PARALLEL:=1
PKG_USE_MIPS16:=0

GO_PKG:=github.com/junegunn/fzf

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/feeds/packages/lang/golang/golang-package.mk

define Package/fzf
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=General-purpose command-line fuzzy finder
  URL:=https://github.com/junegunn/fzf
  DEPENDS:=$(GO_ARCH_DEPENDS)
endef

define Package/fzf/description
  fzf is a general-purpose command-line fuzzy finder.
endef

define Package/fzf/install
	$(call GoPackage/Package/Install/Bin,$(1))
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/bin/fzf-tmux $(1)/usr/bin/fzf-tmux
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/bin/fzf-preview.sh $(1)/usr/bin/fzf-preview.sh
	$(INSTALL_DIR) $(1)/usr/share/fzf/shell
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/shell/* $(1)/usr/share/fzf/shell
endef

$(eval $(call GoBinPackage,fzf))
$(eval $(call BuildPackage,fzf))
