# OvhVmBridger
Bash to ease the setup of vm's on the ovh network 

Currently this only works for CentOs 7

Installation:

pull repo to desired location ie. /usr/bin/

ln -s /usr/bin/OvhVmBridger/configure-ip /usr/bin/configure-ip

Usage:

configure-ip FAILOVER_IP HOST_SERVER_IP IP_VIRTUAL_MAC

running this will replace your network files in: /etc/sysconfig/network-scripts/ and restart your networking
