## General

1. Job description of anyrole related to network that contains **L1, L2, L3, L4**, it doesn't means to experience, rather than that, it refers to that work related to the particular layer in OSI model, like
   | Layer in JD | Layer in OSI | related to |
   |-|-|-|
   || Application layer| within system |
   || Presentation layer| within system |
   || Session layer| within system |
   | L4 | Transport layer| with Cables |
   | L3 | Network layer| with Routers |
   | L2 | Datalink layer| with switches |
   | L1 | Physical layer| with hubs |

   > We remember this layers in order wise,  
   > Place all the words bottom to top, and first letter in each words represents the starting letter of the layers
   >
   > **P**lease **D**o **N**ot **T**ouch **S**afety **P**in **A**lone

## Related to network

1. Full form of ping command is **Packet internet groper**
2. `A` record in DNS server is for **IPv4** and `AAAA` record in DNS server is for **IPv6**
3. **CDR** (Call directory report) / **IPDR** (IP directory report) analysis: Both are the terms refers to legal way of doing to get information like the location, address, time, date, sms, web activities and so on. In one word, it will give you the details about the target's ISP based activity (CDR) and web based activities (IPDR). Both can be view in maltego to get a visual representation using some plugins
4. **SSID** is an abbreviation of _Service set identifier_ or also known as device (Wifi) name
5. **Checksum** in packets are used to check if any data loss is happened or not

## Related to Nmap

1. The default ports being scanned in nmap when without mentioning the ports where **0 to 1023**
2. The `-` in `-p` or `-sV` or `-sC` or anything, the name of the `-` is _tag_

## Related to Exploitation

### Brute-forcing

1. Fuzzing - Giving lot of random datas to the server and make confuse it. Most of the time we do it, in order to know how the server responds

### Reverse shell

1. If the system admin blocks several ports, use **allports** payload to get reverse shell from available opened port

### Honeypot

1. Honeypot is nothing but a trap to catch the hackers
2. If we do setup and keep it online, the hackers will try to attack and gain foothold
3. If they do so, our honeypot will capture the details of the hackers like, IP address, location and so on

## Related to Windows

1. What is Registry?  
   Registry in systems contains the instructions set for doing works. Like if click on any interactive part of gui like the close button **X** button in every software, the registry has instructions that tells the system to close that particular application.

2. What is .dll files?  
   DLL stands for **Dynamic Link Library**. This files are responsible for the syncronization of system registry and customly installed softwares. And if this files were corrupted, it affects only the software.

3. What is .hal files?
   HAL stands for **Hardware Abstraction Layer**. If this files were corrupted, this causes whole system like _BSOD_
