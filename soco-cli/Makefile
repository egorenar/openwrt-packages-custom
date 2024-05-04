#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=soco-cli
PKG_VERSION:=0.4.76
PKG_RELEASE:=1

PYPI_NAME:=soco-cli
PKG_HASH:=052820314587acc17ca64cf1de509b1d9c075f6e4b54a5afb4bae4c7b4c85af2

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/soco-cli
  SECTION:=multimedia
  CATEGORY:=Multimedia
  TITLE:=Powerful command line wrapper for the popular Python SoCo library for controlling Sonos systems
  URL:=https://github.com/avantrec/soco-cli/
  DEPENDS:= \
    +python3-light \
    +python3-soco \
    +python3-xmltodict \
    +python3-ifaddr \
    +python3-tabulate \
    +python3-rangehttpserver \
    +python3-fastapi \
    +python3-uvicorn
endef

define Package/soco-cli/description
  SoCo-CLI is a powerful command line wrapper for the popular Python SoCo library
  for controlling Sonos systems.
endef

$(eval $(call Py3Package,soco-cli))
$(eval $(call BuildPackage,soco-cli))
$(eval $(call BuildPackage,soco-cli-src))
