include $(TOPDIR)/rules.mk

PKG_NAME:=dropwatch
PKG_VERSION:=1.4-7c33d8a8ed105b07a46b55d71d93b36ed34c16db
PKG_RELEASE:=1

PKG_MAINTAINER:=Cristian Morales Vega <cristian@samknows.com>

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=git://git.fedorahosted.org/dropwatch.git 
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=7c33d8a8ed105b07a46b55d71d93b36ed34c16db
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/dropwatch
  SECTION:=net
  CATEGORY:=Network
  TITLE:=dropwatch
  URL:=https://fedorahosted.org/dropwatch/
  DEPENDS:=+libreadline +libnl +libncurses
endef

MAKE_PATH:=src

define Package/dropwatch/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/src/dropwatch $(1)/usr/bin/
endef

$(eval $(call BuildPackage,dropwatch))
