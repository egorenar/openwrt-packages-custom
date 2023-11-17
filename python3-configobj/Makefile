#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-configobj
PKG_VERSION:=5.0.8
PKG_RELEASE:=1

PYPI_NAME:=configobj
PKG_HASH:=6f704434a07dc4f4dc7c9a745172c1cad449feb548febd9f7fe362629c627a97

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-2-Clause
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-configobj
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Config file reading, writing and validation
  URL:=https://github.com/DiffSK/configobj
  DEPENDS:= \
    +python3-light
endef

define Package/python3-configobj/description
 ConfigObj is a simple but powerful config file reader and writer: an ini file round tripper.
 Its main feature is that it is very easy to use, with a straightforward programmer’s interface and
 a simple syntax for config files.
endef

$(eval $(call Py3Package,python3-configobj))
$(eval $(call BuildPackage,python3-configobj))
$(eval $(call BuildPackage,python3-configobj-src))
