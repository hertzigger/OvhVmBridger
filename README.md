# OvhVmBridger
Bash to ease the setup of vm's on the ovh network 

Currently this only works for CentOs 7

Installation:

pull repo to desired location ie. /usr/bin/

ln -s /usr/bin/OvhVmBridger/configure-ip /usr/bin/configure-ip

Usage:

make a note of the INTERFACE_NAME that can be found by looking for a file beginning with ifcfg- in /etc/sysconfig/network-scripts/, use this is place of the INTERFACE_NAME in the following command.

The rest you would probably know if you got here, but FAILOVER_IP is the ip you want to assign to the vm, HOST_SERVER_IP is the server hosting proxmox/vmware and IP_VIRTUAL_MAC you need to generate from your failover ip in the ovh manager.

Remember to generate a vmware mac if you are using vmware.

configure-ip FAILOVER_IP HOST_SERVER_IP IP_VIRTUAL_MAC INTERFACE_NAME

running this will replace your network files in: /etc/sysconfig/network-scripts/ and restart your networking

once this has run you will need to update the mac address on the network interface of the vm in proxmox/vmware and reboot the vm
