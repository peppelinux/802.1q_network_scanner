# 802.1q_network_scanner

It's a simple script that uses these applications

netdiscover, 
vconfig (from vlan suite), 
tshark, 

to solicitate Layer2 activity and sniff vlan headers in background.

It can search a set of network classes or a default networks class set ($DEFAULT_NETWORKS).
You can also edit file variables to customize scanning.

802.1q_network_scanner creates vlan, also start tshark sniffer in background and a netdiscover layer2 scan for each created vlan.
It's pcap outputs, with datetime prefix, could be founded in logs folder and parsed with something like this:

tcpdump -n -r logs/tshark_vlan3.03092016.1743.log.pcap
