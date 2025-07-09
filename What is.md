# What is...?

1. Google dorking:
   - Its like applying filters to our google search results. You can see more in this page Google based Information gathering.
2. Render.com:
   - This is a hosting platform which supports IP logging. So what's IP logging? IP logging is the concept that taking logs of the user's IP addresses. For example, this website hosting platform allows us to do this IP logging. If we host any website in this platform and sets up the IP logging feature, we can able to see every user's IP address who visits our website.
3. Github dorking:
   - Its also like google dorking, but filters for github codes. As we know, github is a platform where we can store our codebase with help of version control system. Dorking in github reveals many misconfigured or sensitive information that are supposed to be private.
4. Non-authoritative result:
   - This result may come from the result of nslookup.
   - As we use this nslookup to know the details of the DNS system, the companies don't just have only one dns server, instead of that they maintain two servers. one is primary server which will always gives us the result and another one secondary server only to backup the primary server when it is down for several reasons.
   - The system administration will always update the dns details only in primary one not the secondary one.
   - The primary server is responsible to update the secondary server, and the process of updating the secondary server is know as zone transfer.
   - So, whenever the primary server is down, and the secondary server replies to our request, this Non-authoritative result will come.
5. Zone transfer in DNS:
   - This can be explained in above paragraph. Refer this
6. SPF:
   - The Sender Policy Framework, is an authentication method used in cybersecurity to verify that incoming emails are sent from authorized servers for a specific domain. This helps prevent email spoofing and phishing attacks, enhancing the security and reputation of the domain.
   - If it is not configured, we can perform some email spoofing attack.
7. ARP table:
   - It is a table that store the IP address and its corresponding MAC address.
   - It usually in switch.