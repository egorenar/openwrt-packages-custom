#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=gallery-dl
PKG_VERSION:=1.26.0
PKG_RELEASE:=1

PYPI_NAME:=gallery_dl
PKG_HASH:=fa0e2d7ebed117daeb8a641c5e1733de8fc2c7dc4b36b4c3575171ed74b187b2

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=Unlicense
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/gallery-dl
  SECTION:=multimedia
  CATEGORY:=Multimedia
  TITLE:=Utility to download images
  URL:=https://github.com/mikf/gallery-dl
  DEPENDS:= \
    +ca-certificates \
    +ffmpeg \
    +yt-dlp \
    +python3-light \
    +python3-pysocks \
    +python3-requests \
    +python3-setuptools
endef

define Package/gallery-dl/description
  gallery-dl is a command-line program to download image galleries and
  collections from several image hosting sites.
endef

$(eval $(call Py3Package,gallery-dl))
$(eval $(call BuildPackage,gallery-dl))
$(eval $(call BuildPackage,gallery-dl-src))
