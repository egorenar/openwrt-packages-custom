#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-mitmproxy-rs
PKG_VERSION:=0.6.3
PKG_RELEASE:=1

PYPI_NAME:=mitmproxy-rs
PYPI_SOURCE_NAME:=mitmproxy_rs
PKG_HASH:=f3b44d255a50573c3b9b71fcb5146841b72ec186208ab2aa3fe35d11add2fd80

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=python-maturin/host

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-mitmproxy-rs
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=This package contains mitmproxy's Rust bits.
  URL:=https://github.com/mitmproxy/mitmproxy_rs
  DEPENDS:= \
    +python3-light \
    $(RUST_ARCH_DEPENDS)
endef

define Package/python3-mitmproxy-rs/description
 This package contains mitmproxy's Rust bits.
endef

$(eval $(call Py3Package,python3-mitmproxy-rs))
$(eval $(call BuildPackage,python3-mitmproxy-rs))
$(eval $(call BuildPackage,python3-mitmproxy-rs-src))
