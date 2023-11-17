#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-cheetah3
PKG_VERSION:=3.2.6.post1
PKG_RELEASE:=1

PYPI_NAME:=Cheetah3
PKG_HASH:=58b5d84e5fbff6cf8e117414b3ea49ef51654c02ee887d155113c5b91d761967

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-cheetah3
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Cheetah is a template engine and code generation tool
  URL:=https://github.com/CheetahTemplate3
  DEPENDS:= \
    +python3-light
endef

define Package/python3-cheetah3/description
 Cheetah3 is a free and open source (MIT) Python template engine. It's a fork of the original CheetahTemplate library.
endef

$(eval $(call Py3Package,python3-cheetah3))
$(eval $(call BuildPackage,python3-cheetah3))
$(eval $(call BuildPackage,python3-cheetah3-src))
