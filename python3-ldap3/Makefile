#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-ldap3
PKG_VERSION:=2.9.1
PKG_RELEASE:=1

PYPI_NAME:=ldap3
PKG_HASH:=f3e7fc4718e3f09dda568b57100095e0ce58633bcabbed8667ce3f8fbaa4229f

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=GPL-3.0-or-later
PKG_LICENSE_FILES:=LICENSE.txt

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-ldap3
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=A strictly RFC 4510 conforming LDAP V3 pure Python client library
  URL:=https://github.com/cannatag/ldap3
  DEPENDS:= \
    +python3-light \
    +python3-pyasn1 \
    +python3-cryptodomex
endef

define Package/python3-ldap3/description
 ldap3 is a strictly RFC 4510 conforming LDAP V3 pure Python client library.
endef

$(eval $(call Py3Package,python3-ldap3))
$(eval $(call BuildPackage,python3-ldap3))
$(eval $(call BuildPackage,python3-ldap3-src))
