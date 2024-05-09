#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-h2
PKG_VERSION:=4.1.0
PKG_RELEASE:=1

PYPI_NAME:=h2
PKG_HASH:=a83aca08fbe7aacb79fec788c9c0bac936343560ed9ec18b82a13a12c28d2abb

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-h2
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=HTTP/2 State-Machine based protocol implementation
  URL:=https://github.com/python-hyper/h2
  DEPENDS:= \
    +python3-light \
    +python3-hpack \
    +python3-hyperframe
endef

define Package/python3-h2/description
 This repository contains a pure-Python implementation of a HTTP/2 protocol stack.
 It's written from the ground up to be embeddable in whatever program you choose to use,
 ensuring that you can speak HTTP/2 regardless of your programming paradigm.
endef

$(eval $(call Py3Package,python3-h2))
$(eval $(call BuildPackage,python3-h2))
$(eval $(call BuildPackage,python3-h2-src))
