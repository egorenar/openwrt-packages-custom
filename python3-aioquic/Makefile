#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python3-aioquic
PKG_VERSION:=1.0.0
PKG_RELEASE:=1

PYPI_NAME:=aioquic
PKG_HASH:=ed31c2b5afa98c5b6cafa4f36149deaf1dff6c5a69701eadd27167415f9f1660

PKG_MAINTAINER:=Alexander Egorenkov <egorenar-dev@posteo.net>
PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-aioquic
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=An implementation of QUIC and HTTP/3
  URL:=https://github.com/aiortc/aioquic
  DEPENDS:= \
    +python3-light \
    +python3-cryptography \
    +python3-certifi \
    +python3-pyopenssl \
    +python3-pylsqpack \
    +python3-service-identity
endef

define Package/python3-aioquic/description
 aioquic is a library for the QUIC network protocol in Python. It features a minimal TLS 1.3 implementation,
 a QUIC stack and an HTTP/3 stack.
endef

$(eval $(call Py3Package,python3-aioquic))
$(eval $(call BuildPackage,python3-aioquic))
$(eval $(call BuildPackage,python3-aioquic-src))
