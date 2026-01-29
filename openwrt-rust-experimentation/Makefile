include $(TOPDIR)/rules.mk

PKG_NAME:=openwrt-rust-experimentation
PKG_VERSION:=1.0.0
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/c03rad0r/openwrt-rust-experimentation.git
PKG_SOURCE_VERSION:=try-manual-build-instructions

include $(INCLUDE_DIR)/package.mk

include $(INCLUDE_DIR)/rust.mk

define Package/openwrt-rust-experimentation
  SECTION:=base
  CATEGORY:=Network
  TITLE:=OpenWrt Rust Experimentation
  MAINTAINER:=c03rad0r
  DEPENDS:=+rust/host
endef

define Package/openwrt-rust-experimentation/description
  An experimental Rust package for OpenWrt.
endef

define Cargo/Configure
  --no-default-features
endef


$(eval $(call RustPackage,openwrt-rust-experimentation))
