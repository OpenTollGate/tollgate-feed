include $(TOPDIR)/rules.mk

PKG_NAME:=nodogsplash
PKG_VERSION:=5.0.0
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/chGoodchild/nodogsplash.git
PKG_SOURCE_VERSION:=increase_username_field
PKG_MIRROR_HASH:=skip

PKG_MAINTAINER:=Your Name <your.email@example.com>
PKG_LICENSE:=GPL-2.0-or-later
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_PARALLEL:=1
PKG_FIXUP:=autoreconf
PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk

define Package/nodogsplash
	SUBMENU:=Captive Portals
	SECTION:=net
	CATEGORY:=Network
	DEPENDS:=+libpthread +iptables-mod-ipopt +libmicrohttpd-no-ssl +libuci
	TITLE:=Open public network gateway daemon
	URL:=https://github.com/chGoodchild/nodogsplash
endef

define Package/nodogsplash/description
	Nodogsplash offers a simple way to open a free hotspot providing
	restricted access to an internet connection. Username field can fit short e-cash notes
endef

define Package/nodogsplash/prepare
	$(PKG_BUILD_DIR)/autogen.sh
endef

define Package/nodogsplash/compile
	$(MAKE) -C $(PKG_BUILD_DIR) all
endef

$(eval $(call BuildPackage,nodogsplash))
