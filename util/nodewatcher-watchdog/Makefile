include $(TOPDIR)/rules.mk

PKG_NAME:=nodewatcher-watchdog
PKG_VERSION:=0.1
PKG_RELEASE:=5

include $(INCLUDE_DIR)/package.mk

define Package/nodewatcher-watchdog
  SECTION:=utils
  CATEGORY:=Utilities
  DEPENDS:=+cronscripts
  TITLE:=nodewatcher-watchdog
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/nodewatcher-watchdog/install
	$(INSTALL_DIR) $(1)/etc/crontabs/run.5
	$(INSTALL_BIN) ./files/check_sanity $(1)/etc/crontabs/run.5/00-check_sanity
	$(INSTALL_BIN) ./files/check_wifi_channel $(1)/etc/crontabs/run.5/01-check_wifi_channel
	$(INSTALL_BIN) ./files/check_ath9k_freeze $(1)/etc/crontabs/run.5/01-check_ath9k_freeze
endef

$(eval $(call BuildPackage,nodewatcher-watchdog))
