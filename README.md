ansible_role_deploy_ww4_nodes
=============================

imports nodes to ww4 from inventory.
creates node profiles

Requirements
------------
Designed for warewulf 4.4

Role Variables
--------------

- `ww4_nodes_group_name`: *ww4_nodes*
  - The host group within inventory to deploy
- `ww4_profiles`:
  - a list of node profiles

Dependencies
------------


Example Playbook
----------------

Example Inventory
-----------------

```
ww4_nodes:
  hosts:
    host3:
      ww4_node_profile: default
      ww4_node_hwaddr: 03:03:03:03:03:03
      ww4_node_ipaddr: 198.51.100.3
    host4:
      ww4_node_profile: default
      ww4_node_hwaddr: 04:04:04:04:04:04
      ww4_node_ipaddr: 198.51.100.4
```

Example node profiles variable:
```
ww4_profiles:
 - Id: 'example-profile-1'
   Comment: 'some comment'
   KernelArgs: 'example kernel=0 args'
   Network:
      netname: netName
      NETMASK: 255.255.0.0
      GATEWAY: 10.1.1.254
 - Id: 'another-example'
   Comment: 'some comment'
   Network:
      NETMASK: 255.255.0.0
      GATEWAY: 10.1.1.254
```


License
-------

BSD

Author Information
------------------

Simppa Äkäslompolo, Aalto Scientific Computing <simppa.akaslompolo@aalto.fi>