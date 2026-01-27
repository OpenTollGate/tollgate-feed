include $(TOPDIR)/rules.mk

PKG_NAME:=openwrt-rust-experimentation
PKG_VERSION:=1.0.0
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/c03rad0r/openwrt-rust-experimentation.git
PKG_SOURCE_VERSION:=main

include $(INCLUDE_DIR)/package.mk

define Package/openwrt-rust-experimentation
  SECTION:=base
  CATEGORY:=Network
  TITLE:=OpenWrt Rust Experimentation
  MAINTAINER:=c03rad0r
endef

define Package/openwrt-rust-experimentation/description
  An experimental Rust package for OpenWrt.
endef

define Build/Compile
	# This is a placeholder. The actual build command for a Rust project is needed here.
	# For example, it might look something like this:
	# (cd $(PKG_BUILD_DIR); cargo build --release)
endef

define Package/openwrt-rust-experimentation/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/target/release/$(PKG_NAME) $(1)/usr/bin/
endef

$(eval $(call BuildPackage,openwrt-rust-experimentation))
