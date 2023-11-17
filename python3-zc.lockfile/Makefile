#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-zc.lockfile
PKG_VERSION:=3.0.post1
PKG_RELEASE:=1

PYPI_NAME:=zc.lockfile
PKG_HASH:=adb2ee6d9e6a2333c91178dcb2c9b96a5744c78edb7712dc784a7d75648e81ec

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=ZPL-2.1
PKG_LICENSE_FILES:=LICENSE.txt

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-zc.lockfile
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Basic inter-process locks
  URL:=https://github.com/zopefoundation/zc.lockfile
  DEPENDS:= \
    +python3-light
endef

define Package/python3-zc.lockfile/description
 The zc.lockfile package provides a basic portable implementation of interprocess locks using lock files.
endef

$(eval $(call Py3Package,python3-zc.lockfile))
$(eval $(call BuildPackage,python3-zc.lockfile))
$(eval $(call BuildPackage,python3-zc.lockfile-src))
