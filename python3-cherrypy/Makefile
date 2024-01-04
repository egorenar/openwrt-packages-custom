#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-cherrypy
PKG_VERSION:=18.9.0
PKG_RELEASE:=1

PYPI_NAME:=CherryPy
PKG_HASH:=6b06c191ce71a86461f30572a1ab57ffc09f43143ba8e42c103c7b3347220eb1

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-2-Clause
PKG_LICENSE_FILES:=LICENSE.md

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-cherrypy
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Object-Oriented HTTP framework
  URL:=https://github.com/cherrypy/cherrypy
  DEPENDS:= \
    +python3-light
endef

define Package/python3-cherrypy/description
 CherryPy is a pythonic, object-oriented HTTP framework.
endef

$(eval $(call Py3Package,python3-cherrypy))
$(eval $(call BuildPackage,python3-cherrypy))
$(eval $(call BuildPackage,python3-cherrypy-src))
