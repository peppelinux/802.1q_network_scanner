# 802.1q_network_scanner

It's a simple script that uses these applications

netdiscover
vconfig (from vlan suite)
tshark

to solicitate Layer2 activity and sniff vlan headers in background.

It can search a set of network classes or a default networks class set ($DEFAULT_NETWORKS), extracted from netdiscover sources.
Edit file variables to customize scanning.

802.1q_network_scanner creates vlan and start tshark sniffer in background and a netdiscover layer2 scan for each one of these.
Its pcap output file could be founded in logs folder, with datetime prefix, and parsed even in realtime with something like this:

tcpdump -n -r logs/tshark_vlan3.03092016.1743.log.pcap
