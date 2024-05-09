#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=mitmproxy
PKG_VERSION:=10.3.0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/mitmproxy/mitmproxy/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=e94362a2a715e2a7def41e4a7a18b61a2ba0233f395776ac81b774b7fee0264d

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/mitmproxy
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Free and open source interactive HTTPS proxy
  URL:=https://mitmproxy.org/
  DEPENDS:= \
    +python3-light \
    +python3-mitmproxy-rs \
    +python3-brotli \
    +python3-click \
    +python3-kaitaistruct \
    +python3-h11 \
    +python3-h2 \
    +python3-hyperframe \
    +python3-aioquic \
    +python3-protobuf \
    +python3-ldap3 \
    +python3-asgiref \
    +python3-certifi \
    +python3-cryptography \
    +python3-flask \
    +python3-msgpack \
    +python3-passlib \
    +python3-pyperclip \
    +python3-urwid-mitmproxy \
    +python3-publicsuffix2 \
    +python3-pyparsing \
    +python3-pyopenssl \
    +python3-ruamel-yaml \
    +python3-sortedcontainers \
    +python3-tornado \
    +python3-typing-extensions \
    +python3-wsproto \
    +python3-zstandard
endef

define Package/mitmproxy/description
 An interactive, SSL/TLS-capable intercepting proxy for HTTP/1, HTTP/2, and WebSockets.
endef

$(eval $(call Py3Package,mitmproxy))
$(eval $(call BuildPackage,mitmproxy))
$(eval $(call BuildPackage,mitmproxy-src))
