#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-cheroot
PKG_VERSION:=10.0.1
PKG_RELEASE:=1

PYPI_NAME:=cheroot
PKG_HASH:=e0b82f797658d26b8613ec8eb563c3b08e6bd6a7921e9d5089bd1175ad1b1740

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-2-Clause
PKG_LICENSE_FILES:=LICENSE.md

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Py3Build/InstallBuildDepends
  $(call HostPython3/PipInstall,--requirement setuptools_scm_git_archive.txt)
endef

define Package/python3-cheroot
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Highly-optimized, pure-python HTTP server
  URL:=https://github.com/cherrypy/cheroot
  DEPENDS:= \
    +python3-light \
    +python3-more-itertools \
    +python3-jaraco.functools
endef

define Package/python3-cheroot/description
 Cheroot is the high-performance, pure-Python HTTP server used by CherryPy.
endef

$(eval $(call Py3Package,python3-cheroot))
$(eval $(call BuildPackage,python3-cheroot))
$(eval $(call BuildPackage,python3-cheroot-src))
