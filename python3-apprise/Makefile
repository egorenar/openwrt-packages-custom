#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-apprise
PKG_VERSION:=1.8.0
PKG_RELEASE:=1

PYPI_NAME:=apprise
PKG_HASH:=e8f58cebfea1a34f569cb4c68809a3175be80ec06f0a2ec473522b92023212c5

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-2-Clause
PKG_LICENSE_FILES:=LICENSE

HOST_PYTHON3_PACKAGE_BUILD_DEPENDS=./babel.txt

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

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
