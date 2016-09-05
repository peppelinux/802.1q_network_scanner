# 802.1q_network_scanner

It's a simple script that uses these applications

netdiscover, 
vconfig (from vlan suite), 
tshark, 

to solicitate Layer2 activity and sniff vlan headers in background.

It can search a set of network classes or a default networks class set ($DEFAULT_NETWORKS).
You can also edit file variables to customize its beahviour.

802.1q_network_scanner creates vlan, it also start tshark sniffer in background and netdiscover layer2 scanning for each scanned vlan. Its pcap output, with datetime prefix, could be found in logs folder and parsed with something like this:

tcpdump -n -r logs/tshark_vlan3.03092016.1743.log.pcap

It doesn't overwrite existing logs, it rename logs folder before start scanning.
