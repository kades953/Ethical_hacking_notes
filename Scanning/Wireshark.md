# What is Wireshark?

Wireshark is a tool that can be used to sniff or capture the packets which is sent and received as every datas is sent and received to/from the internet via packets.

## Colour codes
The red/pink colour says that the packets are sent by our system to the internet or server, where blue colour says that the packets are received by our system from the internet or server.  
Ultimately, we can also change colours in settings

## Filter options
We can use various filter options to view the specific type packets.  
Here are some filters:
- `ip.src==<ip address>`, shows us the packets travel from our system
- `ip.dst==<ip address>`, shows us the packets travel to our system
- `ip.addr==<ip address>`, shows us the packets that associated to that particular ip address