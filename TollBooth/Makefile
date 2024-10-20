include $(TOPDIR)/rules.mk

PKG_NAME:=TollBooth
PKG_VERSION:=1.0
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/OpenTollGate/TollBooth.git
PKG_SOURCE_VERSION:=main
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Captive Portals
  TITLE:=Tollbooth
  DEPENDS:=+uhttpd +uhttpd-mod-lua +lua +lua-cjson
endef

define Package/$(PKG_NAME)/description
  Backend plugin providing API endpoints for the captive portal.
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Compile
	# Nothing to compile
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/lib/lua/tollbooth
	$(INSTALL_DATA) ./files/dummy.lua $(1)/usr/lib/lua/tollbooth/
endef


$(eval $(call BuildPackage,$(PKG_NAME)))
