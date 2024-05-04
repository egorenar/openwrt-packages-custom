#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-oauthlib
PKG_VERSION:=3.2.2
PKG_RELEASE:=1

PYPI_NAME:=oauthlib
PKG_HASH:=9859c40929662bec5d64f34d01c99e093149682a3f38915dc0655d5a633dd918

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-oauthlib
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=A generic, spec-compliant, thorough implementation of the OAuth request-signing logic
  URL:=https://github.com/oauthlib/oauthlib
  DEPENDS:= \
    +python3-light \
    +python3-cryptography \
    +python3-blinker \
    +python3-jwt
endef

define Package/python3-oauthlib/description
 A generic, spec-compliant, thorough implementation of the OAuth request-signing logic for Python 3.8+.
endef

$(eval $(call Py3Package,python3-oauthlib))
$(eval $(call BuildPackage,python3-oauthlib))
$(eval $(call BuildPackage,python3-oauthlib-src))
