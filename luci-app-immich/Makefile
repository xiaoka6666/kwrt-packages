

include $(TOPDIR)/rules.mk


LUCI_TITLE:=LuCI support for Immich
LUCI_PKGARCH:=all
LUCI_DEPENDS:=+lsblk +docker +dockerd +luci-lib-taskd +luci-lib-docker +docker-compose

define Package/luci-app-immich/conffiles
/etc/config/immich
endef

define Package/luci-app-immich/prerm
#!/bin/sh
/usr/libexec/istorec/immich.sh stop
exit 0
endef

include $(TOPDIR)/feeds/luci/luci.mk

# call BuildPackage - OpenWrt buildroot signature
