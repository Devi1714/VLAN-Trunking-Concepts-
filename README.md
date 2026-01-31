# VLAN-Trunking-Concepts-
🌐📘 Teaching VLAN &amp; Trunking Concepts – CCNA Networking 🔀
without trunk - separate wires for each vlan :
 
Switch>enable
Switch#conf t
Switch(config)#vlan 2
Switch(config-vlan)#name Manager
Switch(config-vlan)#exit
Switch(config)#vlan 3
Switch(config-vlan)#name TL
Switch(config-vlan)#exit
Switch(config)#vlan 4
Switch(config-vlan)#name staff
Switch(config-vlan)#exit
Switch(config)#interface fa0/2
Switch(config-if)#switchport mode ?
  access   Set trunking mode to ACCESS unconditionally
  dynamic  Set trunking mode to dynamically negotiate access or trunk mode
  trunk    Set trunking mode to TRUNK unconditionally
Switch(config-if)#switchport access vlan 2
Switch(config-if)#exit 
Switch(config)#int fa0/3
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 3
Switch(config-if)#exit 
Switch(config)#int fa0/4
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 4
Switch(config-if)#exit 
Switch(config)#int fa0/6
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 2
Switch(config-if)#exit 
Switch(config)#int fa0/7
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 3
Switch(config-if)#exit 
Switch(config)#int fa0/8
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 4
Switch(config-if)#exit 
