include $(TOPDIR)/rules.mk

PKG_NAME:=tollgate-module-basic-go
PKG_VERSION:=1.0.0
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/OpenTollGate/tollgate-module-basic-go.git
PKG_SOURCE_VERSION:=main

include $(INCLUDE_DIR)/package.mk

define Package/tollgate-module-basic-go
  SECTION:=base
  CATEGORY:=Network
  TITLE:=Tollgate Basic Go Module
  MAINTAINER:=c03rad0r^3
endef

define Package/tollgate-module-basic-go/description
  A basic Go module for the Tollgate project.
endef

define Build/Compile
	# This is a placeholder. The actual build command for a Go project is needed here.
	# For example, it might look something like this:
	# (cd $(PKG_BUILD_DIR); go build -o $(PKG_NAME))
endef

define Package/tollgate-module-basic-go/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/$(PKG_NAME) $(1)/usr/bin/
endef

$(eval $(call BuildPackage,tollgate-module-basic-go))
