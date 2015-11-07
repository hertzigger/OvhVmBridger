# OvhVmBridger
Bash to ease the setup of vm's on the ovh network 

Currently this only works for CentOs 7

Installation:

pull repo to desired location ie. /usr/bin/

ln -s configure-ip OvhVmBridger/configure-ip

Usage:

./configure-ip <FAILOVER IP> <HOST SERVER IP> <IP VIRTUAL MAC>

running this will replace your network files in: /etc/sysconfig/network-scripts/ and restart your networking
