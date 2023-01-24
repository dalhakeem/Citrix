# Citrix ADC (NetScaler) Commands Cheatsheet

## Show Commands

- Show system information: `show system`
- Show system resources: `show system resources`
- Show interfaces: `show interface`
- Show routing table: `show ip route`
- Show VPN sessions: `show vpn session`
- Show SSL certificate bindings: `show ssl certkey binding`
- Show configuration: `show ns config`

## Configuration Commands

- Enable/disable a feature: `enable/disable feature <feature name>`
- Add a new IP address: `add ns ip <IP_address> <netmask>`
- Add a new route: `add route <destination> <netmask> <gateway>`
- Add a new service: `add service <name> <IP_address> <port>`
- Add a new virtual server: `add lb vserver <name> <service_type> <IP_address> <port>`
- Bind a service to a virtual server: `bind lb vserver <vserver_name> <service_name>`
- Save configuration: `save ns config`

## Troubleshooting Commands

- Show current connections: `show ns conn`
- Show connection details: `show ns conn -detail`
- Show connection count by IP: `show ns conn count -byip`
- Show system events: `show events`
- Show system statistics: `show stat`
- Show system parameters: `show ns param`
- Show system performance: `show ns performance`
