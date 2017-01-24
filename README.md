Networking
=========

This role statically defines variables on the network-layer like default gateway and dns-servers. It basically takes over the tasks of the options-field from a DHCP-server. It's meant for lab-environments.

Requirements
------------

There is no possibility to assign IP's. This must be done using the vagratn file. <br>
Tested on CentOS

Role Variables
--------------

| variable        | default           | Description  |
| ------------- |:-------------:| -----:|
|networking    | yes | boolean |
| hostname    | centos      |   name of the server |
| gateway    | /      |   ip of the gateway |
| nameserver    | /      |  enumeration from ip's from dns-servers |

Dependencies
------------

No dependencies

Example Playbook
----------------
```
dnsserver:
  - 192.0.2.254
  - 172.16.255.254

hostname: 'workstation'
defaultgateway: '192.0.2.254'
```
Author Information
------------------

Written by Thomas Detemmerman to support in a lab-environment.
