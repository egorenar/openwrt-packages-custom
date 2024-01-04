#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-feedparser
PKG_VERSION:=6.0.11
PKG_RELEASE:=1

PYPI_NAME:=feedparser
PKG_HASH:=c9d0407b64c6f2a065d0ebb292c2b35c01050cc0dc33757461aaabdc4c4184d5

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-2-Clause
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-feedparser
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Universal feed parser, handles RSS 0.9x, RSS 1.0, RSS 2.0, CDF, Atom 0.3, and Atom 1.0 feeds
  URL:=https://github.com/kurtmckee/feedparser
  DEPENDS:= \
    +python3-light \
    +python3-sgmllib3k \
    +python3-requests
endef

define Package/python3-feedparser/description
 feedparser - Parse Atom and RSS feeds in Python.
endef

$(eval $(call Py3Package,python3-feedparser))
$(eval $(call BuildPackage,python3-feedparser))
$(eval $(call BuildPackage,python3-feedparser-src))
