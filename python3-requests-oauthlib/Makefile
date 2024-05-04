#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-requests-oauthlib
PKG_VERSION:=2.0.0
PKG_RELEASE:=1

PYPI_NAME:=requests-oauthlib
PKG_HASH:=b3dffaebd884d8cd778494369603a9e7b58d29111bf6b41bdc2dcd87203af4e9

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=ISC
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-requests-oauthlib
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=OAuthlib authentication support for Requests
  URL:=https://github.com/requests/requests-oauthlib
  DEPENDS:= \
    +python3-light \
    +python3-requests \
    +python3-oauthlib
endef

define Package/python3-requests-oauthlib/description
 This project provides first-class OAuth library support for Requests.
endef

$(eval $(call Py3Package,python3-requests-oauthlib))
$(eval $(call BuildPackage,python3-requests-oauthlib))
$(eval $(call BuildPackage,python3-requests-oauthlib-src))
