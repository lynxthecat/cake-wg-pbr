# cake-wg-pbr
Set up CAKE in the context of WireGuard with PBR

Relies on skb->hash preservation, see: 

https://lists.bufferbloat.net/pipermail/cake/2020-May/005257.html

And capturing ingress packets from layer 3 WireGuard interface, see: 

https://forum.openwrt.org/t/nftables-and-qos-in-2021/112013/517

## Required packages

This cake-wg-pbr script requires at least the following packages:

- **tc-tiny**
- **kmod-ifb**
- **kmod-sched-core**
- **kmod-sched-cake**

## Installation on OpenWrt

To install:

  ```bash
   opkg update; opkg install tc-tiny kmod-ifb kmod-sched-core kmod-sched-cake
   cd /etc/init.d/
   wget https://raw.githubusercontent.com/lynxthecat/cake-wg-pbr/main/cake-wg-pbr
   chmod +x ./cake-wg-pbr
   cd /etc/hotplug.d/iface/
   wget https://raw.githubusercontent.com/lynxthecat/cake-wg-pbr/main/11-cake-wg-pbr
   chmod +x ./11-cake-wg-pbr
   ```
   
   Set the WAN and VPN interfaces in cake-wg-pbr
