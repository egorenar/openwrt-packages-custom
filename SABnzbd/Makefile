#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=SABnzbd
PKG_VERSION:=4.3.3
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-src.tar.gz
PKG_SOURCE_URL:=https://github.com/sabnzbd/sabnzbd/releases/download/$(PKG_VERSION)/
PKG_HASH:=3f787e9734e22bc69f6c160949d93bfd5ef824fe72b74a50eac356ec2262345f

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=GPL-2.0-or-later
PKG_LICENSE_FILES:=LICENSE.txt

include $(INCLUDE_DIR)/package.mk

define Package/SABnzbd
  SECTION:=net
  CATEGORY:=Network
  TITLE:=The automated Usenet download tool
  URL:=https://github.com/sabnzbd/sabnzbd
  DEPENDS:= \
    +python3-light \
    +python3-rebulk \
    +python3-babelfish \
    +python3-guessit \
    +python3-puremagic \
    +python3-pysocks \
    +python3-chardet \
    +python3-portend \
    +python3-sgmllib3k \
    +python3-pytz \
    +python3-tempora \
    +python3-dateutil \
    +python3-zc.lockfile \
    +python3-more-itertools \
    +python3-jaraco.context \
    +python3-jaraco.classes \
    +python3-jaraco.text \
    +python3-jaraco.collections \
    +python3-jaraco.functools \
    +python3-cherrypy \
    +python3-six \
    +python3-cheroot \
    +python3-configobj \
    +python3-feedparser \
    +python3-pycparser \
    +python3-cffi \
    +python3-cheetah3 \
    +python3-sabctools \
    +python3-cryptography \
    +python3-ujson \
    +python3-apprise \
    +@BUSYBOX_CONFIG_IONICE \
    +unrar \
    +unzip \
    +p7zip \
    +curl \
    +par2cmdline-turbo
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/SABnzbd/install
	$(INSTALL_DIR) $(1)/usr/lib/SABnzbd
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/SABnzbd.py $(1)/usr/lib/SABnzbd
	$(CP) -R $(PKG_BUILD_DIR)/email $(1)/usr/lib/SABnzbd
	$(CP) -R $(PKG_BUILD_DIR)/icons $(1)/usr/lib/SABnzbd
	$(CP) -R $(PKG_BUILD_DIR)/interfaces $(1)/usr/lib/SABnzbd
	$(CP) -R $(PKG_BUILD_DIR)/locale $(1)/usr/lib/SABnzbd
	$(CP) -R $(PKG_BUILD_DIR)/po $(1)/usr/lib/SABnzbd
	$(CP) -R $(PKG_BUILD_DIR)/sabnzbd $(1)/usr/lib/SABnzbd
	$(CP) -R $(PKG_BUILD_DIR)/scripts $(1)/usr/lib/SABnzbd
	$(CP) -R $(PKG_BUILD_DIR)/tools $(1)/usr/lib/SABnzbd

	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) ./files/sabnzbd.init $(1)/etc/init.d/sabnzbd
endef

define Package/SABnzbd/description
 SABnzbd is an Open Source Binary Newsreader written in Python.
endef

$(eval $(call BuildPackage,SABnzbd))
