#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-publicsuffix2
PKG_VERSION:=2.20191221
PKG_RELEASE:=1

PYPI_NAME:=publicsuffix2
PKG_HASH:=00f8cc31aa8d0d5592a5ced19cccba7de428ebca985db26ac852d920ddd6fe7b

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=Custom
PKG_LICENSE_FILES:=publicsuffix2.LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Py3Build/InstallBuildDepends
  $(call HostPython3/PipInstall,--requirement requests.txt)
endef

define Package/python3-publicsuffix2
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Get a public suffix for a domain name using the Public Suffix List
  URL:=https://github.com/nexB/python-publicsuffix2
  DEPENDS:= \
    +python3-light
endef

define Package/python3-publicsuffix2/description
 Get a public suffix for a domain name using the Public Suffix List.
 Forked from and using the same API as the publicsuffix package.
endef

$(eval $(call Py3Package,python3-publicsuffix2))
$(eval $(call BuildPackage,python3-publicsuffix2))
$(eval $(call BuildPackage,python3-publicsuffix2-src))
