#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=gallery-dl
PKG_VERSION:=1.27.3
PKG_RELEASE:=1

PYPI_NAME:=gallery_dl
PKG_HASH:=20b9e76e7422267041395f3b996c35c4753c0ed097215570470cff3dfcd54922

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=GPL-2.0-or-later
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
    +python3-requests
endef

define Package/gallery-dl/description
  gallery-dl is a command-line program to download image galleries and
  collections from several image hosting sites.
endef

$(eval $(call Py3Package,gallery-dl))
$(eval $(call BuildPackage,gallery-dl))
$(eval $(call BuildPackage,gallery-dl-src))
