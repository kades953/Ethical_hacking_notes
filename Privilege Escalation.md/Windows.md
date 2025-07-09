# Tips to escalate our privilege in Windows:

### 1. Initial Enumeration:

#### Sytem Enumeration

- `help` - to list available commands
- `systeminfo` - to get system information
- `wmic` - **Windows Management Instrumentation Command line** Tells us more about the machine in cli, more like root & we do know lot more informations with these
- `wmic qfe` - **Quick fix Engineering** to know what patches installed and when (this will not work in every machines)
- `wmic logicaldisk get caption,description` - This will return the available disks like C drive, D drive etc

#### User Enumeration

- `whoami /priv` - like _sudo -l_
- `net user` - to list all the users in that machine
- `net user <username>` - to get additional information about the particular user

#### Network Enumeration

- `ipconfig /all` - Returns IP related information with extra informations
- `arp -a` - ARP table
- `route print` - prints route tables
- `netstat -ano` - displays what ports are opened that are not reveled in our scanning

#### Password Hunting

- `findstr /si password *.txt` - finds the word password in all .txt files in current directory
- Check out few more commands in **PayloadAllTheThings** that mentioned below

#### AntiVirus Enumeration

- `sc query windefend` - _sc_ stands for _service control_. It used for get the particular service information
- `sc queryex type= service` - returns all running services
- `netsh firewall show state` - returns firewall status

### 2. Some Automated tools:

#### Executables,

- winPEAS.exe
- Seatbelt.exe (compile)
- Watson.exe (compile)
- SharpUp.exe (compile)

#### PowerShell,

- Sherlock.ps1
- PowerUp.ps1
- jaws-enum.ps1

#### Others,

- windows-exploit-suggester.py (local) - upload and enter command `winpeas.exe`
- Exploit Suggester (Metasploit) - to run this `run post/multi/recon/local_exploit_suggester`

### 3. Kernel Exploits:

- Visit **windows-kernel-exploits** by SecWiki in github
- [With Metasploit] First, run a [exploit suggester](#others), then copy the relevent exploit module that came out of the result, then `background` the current session, then use that copied exploit, set all the required options and set the session. Then exploit.
- [Manual method] Use **winPEAS** or **windows-exploit-suggester.py** to get to know which exploit should we use to escalate, download that exploit, transfer it to victim machine, run it

### 4. Passwords and Port forwarding:

---

### Some intresting informations:

1. The system level user of windows is commonly known as **NT AUTHORITY\SYSTEM**
2. Check out fuzzy security website to know more about hacking
3. Visit **PayloadAllTheThings or InternalAllTheThings by user swisskyrepo** in github, for some paylods
4. Also check **hacktricks** website
5. You can visit **windows-kernel-exploits** by SecWiki in github
