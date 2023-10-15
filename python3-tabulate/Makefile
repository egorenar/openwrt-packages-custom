#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-tabulate
PKG_VERSION:=0.9.0
PKG_RELEASE:=1

PYPI_NAME:=tabulate
PKG_HASH:=0095b12bf5966de529c0feb1fa08671671b3368eec77d7ef7ab114be2c068b3c

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-tabulate
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Pretty-print tabular data in Python
  URL:=https://github.com/astanin/python-tabulate/
  DEPENDS:= \
    +python3-light
endef

define Package/python3-tabulate/description
  Pretty-print tabular data in Python, a library and a command-line utility.
endef

$(eval $(call Py3Package,python3-tabulate))
$(eval $(call BuildPackage,python3-tabulate))
$(eval $(call BuildPackage,python3-tabulate-src))
