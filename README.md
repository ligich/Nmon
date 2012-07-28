Nmon
====

Nmon: Network Monitor. Python program that monitor the network in Python.
This program has been done for a University project about network scanning.
Original article: http://robindavid.comli.com/nmon-network-monitor/

How it works ?
--------------

The module is mainly articulated around a modified version of python-nmap made by Alexandre Norman http://code.google.com/p/python-nmap/.
Indeed I needed to gather the hole nmap output MAC, OS, and services included whereas it is not possible for now.
So basically you just need to do:
    import nmon
    nmon.runMonitor(“192.168.0.*”)

Note: Change the IP to address to match you local network

So basically once you have done this two commands the monitor run in the background and monitor the network. At any time you can query it to get the network state available hosts etc.
The monitor maintain a list of hosts even if they disconnect of the network. This allow to know when an host has disconected for instance.
For a given host you can retrieve multiples informations like IP, MAC, OS, ports and services, uptime (basically all the informations that nmap can gather).
The network and hosts are regularly scanned, so this program create a really important packet throughput on the network. Be careful this module might
trigger some NIDS alerts.

For more informations check the article given at the url above.