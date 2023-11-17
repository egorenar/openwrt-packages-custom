#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-sgmllib3k
PKG_VERSION:=1.0.0
PKG_RELEASE:=1

PYPI_NAME:=sgmllib3k
PKG_HASH:=7868fb1c8bfa764c1ac563d3cf369c381d1325d36124933a726f29fcdaa812e9

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-2-Clause
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-sgmllib3k
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Py3k port of sgmllib
  URL:=http://hg.hardcoded.net/sgmllib
  DEPENDS:= \
    +python3-light
endef

define Package/python3-sgmllib3k/description
 sgmllib was dropped in Python 3. For those depending on it, that’s somewhat unfortunate.
 This is a quick and dirty port of this old module. I just ran 2to3 on it and published it.
 I don’t intend to maintain it, so it might be a good idea to eventually think about finding another module to use.
endef

$(eval $(call Py3Package,python3-sgmllib3k))
$(eval $(call BuildPackage,python3-sgmllib3k))
$(eval $(call BuildPackage,python3-sgmllib3k-src))
