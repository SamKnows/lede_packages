#
# Copyright (C) 2007-2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=traceroute
PKG_VERSION:=2.1.0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=@SF/traceroute
PKG_MD5SUM:=84d329d67abc3fb83fc8cb12aeaddaba

PKG_MAINTAINER:=Cristian Morales Vega <cristian@samknows.com>
PKG_LICENSE:=GPL-2.0+

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/traceroute
  SECTION:=net
  CATEGORY:=Network
  TITLE:=traceroute
  URL:=http://sourceforge.net/projects/traceroute/
endef

define Package/traceroute/description
 New implementation of the traceroute utility for modern Linux systems
endef

define Build/Compile
	$(call Build/Compile/Default, $(MAKE_VARS))
endef

define Package/traceroute/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/traceroute/traceroute $(1)/usr/bin/
endef

$(eval $(call BuildPackage,traceroute))
