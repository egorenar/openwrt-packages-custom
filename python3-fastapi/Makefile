#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-fastapi
PKG_VERSION:=0.103.2
PKG_RELEASE:=1

PYPI_NAME:=fastapi
PKG_HASH:=75a11f6bfb8fc4d2bec0bd710c2d5f2829659c0e8c0afd5560fdda6ce25ec653

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-fastapi
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Modern, fast (high-performance), web framework for building APIs
  URL:=https://github.com/tiangolo/fastapi/
  DEPENDS:= \
    +python3-light \
    +python3-uvicorn
endef

define Package/python3-fastapi/description
  FastAPI is a modern, fast (high-performance), web framework for building APIs with Python 3.7+
  based on standard Python type hints.
endef

$(eval $(call Py3Package,python3-fastapi))
$(eval $(call BuildPackage,python3-fastapi))
$(eval $(call BuildPackage,python3-fastapi-src))
