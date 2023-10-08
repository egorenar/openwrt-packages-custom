#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=streamlink
PKG_VERSION:=3.2.0
PKG_RELEASE:=1

PYPI_NAME:=streamlink
PKG_HASH:=9770d2d83844c5378a73e14130dcb760abc856566caa0a41fc5b97a0ded5d926

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=Unlicense
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/streamlink
  SECTION:=multimedia
  CATEGORY:=Multimedia
  TITLE:=Utility to pipe video streams into a video player
  URL:=https://github.com/streamlink/streamlink
  DEPENDS:= \
    +ca-certificates \
    +ffmpeg \
    +python3-light \
    +python3-requests \
    +python3-charset-normalizer \
    +python3-pysocks \
    +python3-lxml \
    +python3-cryptodome \
    +python3-websocket-client \
    +python3-pycountry \
    +python3-isodate \
    +python3-setuptools
endef

define Package/streamlink/description
  Streamlink is a CLI utility which pipes video streams from various
  services into a video player, such as VLC. The main purpose of
  streamlink is to avoid resource-heavy and unoptimized websites,
  while still allowing the user to enjoy various streamed content.
endef

$(eval $(call Py3Package,streamlink))
$(eval $(call BuildPackage,streamlink))
$(eval $(call BuildPackage,streamlink-src))
