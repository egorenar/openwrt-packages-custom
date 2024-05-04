#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-jwt
PKG_VERSION:=2.8.0
PKG_RELEASE:=1

PYPI_NAME:=PyJWT
PKG_HASH:=57e28d156e3d5c10088e0c68abb90bfac3df82b40a71bd0daa20c65ccd5c23de

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-jwt
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=JSON Web Token implementation in Python
  URL:=https://github.com/jpadilla/pyjwt
  DEPENDS:= \
    +python3-light \
    +python3-cryptography
endef

define Package/python3-jwt/description
 A Python implementation of RFC 7519.
endef

$(eval $(call Py3Package,python3-jwt))
$(eval $(call BuildPackage,python3-jwt))
$(eval $(call BuildPackage,python3-jwt-src))
