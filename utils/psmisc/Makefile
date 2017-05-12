include $(TOPDIR)/rules.mk

PKG_NAME:=psmisc
PKG_VERSION:=22.21
PKG_RELEASE:=1

PKG_SOURCE:=psmisc-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=@SF/psmisc
PKG_HASH:=97323cad619210845b696d7d722c383852b2acb5c49b5b0852c4f29c77a8145a

PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk

define Package/psmisc
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=proc utilities
  URL:=https://gitlab.com/psmisc/psmisc
endef

define Package/psmisc/description
  psmisc is a set of additional small useful utilities that use
  the proc filesystem: killall and prtstat
endef

CONFIGURE_ARGS += \
	--disable-harden-flags

define Package/psmisc/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) \
		$(PKG_INSTALL_DIR)/usr/bin/{killall,prtstat} \
		$(1)/usr/bin/
endef

$(eval $(call BuildPackage,psmisc))
