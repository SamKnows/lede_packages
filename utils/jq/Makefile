include $(TOPDIR)/rules.mk

PKG_NAME:=jq
PKG_VERSION:=1.5
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/stedolan/jq/releases/download/jq-$(PKG_VERSION)/
PKG_HASH:=c4d2bfec6436341113419debf479d833692cc5cdab7eb0326b5a4d4fbe9f493c
PKG_MAINTAINER:=Cristian Morales Vega <cristian@samknows.com>

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/jq
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=jq
  URL:=https://stedolan.github.io/jq/
endef

define Package/jq/description
 jq
endef

TARGET_CFLAGS += -ffunction-sections -fdata-sections -flto
TARGET_LDFLAGS += -Wl,--gc-sections -Wl,--as-needed

# https://github.com/Entware-ng/Entware-ng/issues/294
TARGET_CFLAGS += -fno-ipa-sra

define Package/jq/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/jq $(1)/usr/bin/
endef

$(eval $(call BuildPackage,jq))
