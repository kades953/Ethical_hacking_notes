# What is Nmap?

If we run Nmap within LAN, it will give you all the hosts connected to the device.  
But if we run Nmap out-of-LAN, it will not give you the connected hosts, instead of that, it will give you the details of the device assigned with the IP address. And that is called spear scanning.

## Scan types,

- -sT: TCP connect scan, Initiate the tcp 3-way handshake and give you the result from the ACK packet came from the target
- -sS: Stealth scan, same as TCP connect scan, but it will not send the ack packet to the target, prevents the detection
- -sV: Version scan
- -sU: UDP scan
- -A: Aggressive scan, runs all scan including -sV, -sC, -O, tracert scan, making more noise in the network
- -T<1-5>: Timing scan, 1 is slower and 5 is faster. Default is T3 (speed will trigger the alarm in firewall and slow will not trigger)