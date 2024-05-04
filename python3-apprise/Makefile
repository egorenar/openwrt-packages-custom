#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-apprise
PKG_VERSION:=1.7.6
PKG_RELEASE:=1

PYPI_NAME:=apprise
PKG_HASH:=077f09309cc8a6c9063dbd614b343807d527d546693b7fe8fc5a4433502fea6c

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-2-Clause
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Py3Build/InstallBuildDepends
  $(call HostPython3/PipInstall,--requirement babel.txt)
endef

define Package/python3-apprise
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Push Notifications that work with just about every platform
  URL:=https://github.com/caronc/apprise
  DEPENDS:= \
    +python3-light \
    +python3-requests \
    +python3-requests-oauthlib \
    +python3-click \
    +python3-markdown \
    +python3-yaml \
    +python3-certifi
endef

define Package/python3-apprise/description
 Apprise allows you to send a notification to almost all of the most popular notification
 services available to us today such as: Telegram, Discord, Slack, Amazon SNS, Gotify, etc.
endef

$(eval $(call Py3Package,python3-apprise))
$(eval $(call BuildPackage,python3-apprise))
$(eval $(call BuildPackage,python3-apprise-src))
