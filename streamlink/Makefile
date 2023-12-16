#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=streamlink
PKG_VERSION:=6.5.0
PKG_RELEASE:=1

PYPI_NAME:=streamlink
PKG_HASH:=8f4d61593bcce10f8d5e84ca956aac4fa639c0a349e7df379834373a883966ed

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-2-Clause
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Py3Build/InstallBuildDepends
  $(call HostPython3/PipInstall,--requirement versioningit.txt)
endef

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
    +python3-pysocks \
    +python3-lxml \
    +python3-cryptodome \
    +python3-websocket-client \
    +python3-pycountry \
    +python3-isodate \
    +python3-certifi \
    +python3-trio \
    +python3-trio-websocket \
    +python3-typing-extensions \
    +python3-urllib3
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
