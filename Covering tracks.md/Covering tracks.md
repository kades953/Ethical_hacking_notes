# Covering tracks

This is process of removing/erasing/clearing the tracks we made in the target machine. Every system takes logs that what all are the process were done in the system. If we take a foothold in the target machine, the target machine will record all the things we made in that machine. So clearing the logs is a good way to being untracked.

### What should we do

1. Before attack,

   - Mask our IP address, by
     - setup a **proxy** via browser settings or
     - using any VPN like **hola VPN** or
     - using softwares like **ultrasurf** or
     - using tools like **zerotrace**
   - Mask our MAC address, by
     - using **technitium/SMAC** tools to generate random MAC address or
     - using **MAC changer** tool
   - Operating System
     - always use **live OS** (from USB)
     - prefer to use **Tails OS**, it offers a better anonymity and privacy tools
   - for browser
     - use **Tor**

2. When attacking,

   - install any preferred **backdoors** (use public IP address and non-common or system ports)
     - like php reverse shell
     - netcat listener
     - or anything you prefer

3. After attack,
   - remove tracks or logs from,
     - if you have gui,
       - dxdiag
       - msinfo32
       - eventvwr.msc
     - if you have cli
       - In windows cmd, `del *.log /a /s /q /f`

### Tools can be used

- stellar bitracer
