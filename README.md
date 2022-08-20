# ServerSync

The work in progress incredible server syncing plugin that links multiple servers into one.

**Modules include:**
- ServerSync-Bukkit
- ServerSync-Velocity (for single proxy use & load balancing)
- ServerSync-Manager (for multiple proxy routing)

*Please note: if you do wish to use this software across proxies then you will need the Velocity plugin itself as well as the manager, they work together to gain an accurate player count and load balance accordingly.*

**How does Load balancing work across multiple proxies?**

Simply put: it doesn't. You will need an external load balancer to do this such as TCPShield or CosmicGuard.

The only reason for the manager is to determine where players should go in a multiple proxy environment where the actual servers playercount can be difficult to fetch.
Also: the manager is not a plugin, it is a separate program that runs on the server.

The proxy plugin also provides a few extra features such as:
- Automatic server adding / detection (configurable)
- Automatic server removal (configurable)
- Automatic server restart (configurable)
- Global player count syncing across all proxies (configurable)
- Automatic load balancing groups not just specific to actual synced servers.

You can expect a functioning version ready for production by the end of 2022. I will publish this plugin as a paid resource on Spigot or another site, but will leave the source code here for those who know how to build it.

TODO:
- [ ] Create the shared communication functions
- [ ] Create the Bukkit module
- [ ] Create the Velocity module
- [ ] Create the Manager module

TODO Functionality:
- [ ] Add automatic server adding / removal
- [ ] Add automatic server restart
- [ ] Add automatic player count syncing
- [ ] Add automatic load balancing across multiple proxies
- [ ] Add automatic load balancing groups not just specific to actual synced servers.

Building:
1) Clone the project
2) Run `mvn clean install`