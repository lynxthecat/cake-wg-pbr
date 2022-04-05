# cake-wg-pbr
Set up CAKE in the context of WireGuard with PBR

## Required packages

This cake-wg-pbr script supports setting up CAKE with only the following package:

- **tc-tiny** 


## Installation on OpenWrt

To install:

  ```bash
   opkg update; opkg install tc-tiny
   cd /etc/init.d/
   wget https://raw.githubusercontent.com/lynxthecat/cake-wg-pbr/main/cake-wg-pbr
   chmod +x ./cake-wg-pbr
   cd /etc/hotplud.g/iface/
   wget https://raw.githubusercontent.com/lynxthecat/cake-wg-pbr/main/11-cake-wg-pbr
   chmod +x ./11-cake-wg-pbr
   ```
   
   Set the WAN and VPN interfaces in cake-wg-pbr
