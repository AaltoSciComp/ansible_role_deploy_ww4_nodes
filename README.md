ansible_role_deploy_ww4_nodes
=============================

imports nodes to ww4 from inventory.

Requirements
------------
Designed for warewulf 4.4

Role Variables
--------------

- `ww4_nodes_group_name`: *ww4_nodes*
  - The host group from inventory to deploy

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


License
-------

BSD

Author Information
------------------

Simppa Äkäslompolo, Aalto Scientific Computing <simppa.akaslompolo@aalto.fi>