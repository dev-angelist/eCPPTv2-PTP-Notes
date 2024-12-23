# 🛣️ RoadMap & My Experience

[![](https://github.com/sidneysimas/eCPPTv2-PTP-Notes/raw/main/.gitbook/assets/image%20\(1\).png)](https://github.com/sidneysimas/eCPPTv2-PTP-Notes/blob/main/.gitbook/assets/image%20\(1\).png)

The path to becoming a penetration tester is like a winding river, ever-changing and unpredictable. To navigate it, one must be adaptable, resourceful, and always willing to learn.

The journey to becoming a penetration tester is a lifelong one. It is a journey of continuous learning, discovery, and self-improvement.

I'm writing this '[review](https://medium.com/@dev-angelist/learning-path-my-experience-for-the-eccptv2-ptp-certification-april-2024-15ddf6b29a8f)' to assist aspiring candidates in their journey towards obtaining the eCPPTv2 certification. My aim is to share the resources, insights, and tools essential for preparation, offering advice and addressing common concerns. Unlike the **eJPTv2** exam, where you have a only two days to tackle everything alongside multiple-choice questions, the eCPPTv2 certification presents a different challenge. This exam grants you a generous timeframe of 7 days to compromise the entire environment and an additional 7 days to compile a comprehensive professional report detailing all identified vulnerabilities, their criticality, and proposed resolutions.

While seven days may seem ample, completing the exam in less time is entirely feasible. Personally, I managed to conquer it within four days, allowing myself one day of respite, and dedicated two days to crafting a detailed report spanning a total of 80 pages. Is it worth the effort? Undoubtedly. The eCPPTv2 certification rigorously evaluates your prowess in **pivoting**, **buffer overflow** exploits, and, most importantly, your comprehension of the pentesting process. Success hinges not on merely reaching the root but on uncovering every **vulnerability** within the environment. Hence, a robust methodology and thorough enumeration are indispensable. Unlike conventional **CTF** challenges, you won’t find user.txt or root.txt flags; instead, you’ll encounter files containing crucial information such as passwords, IPs, or network segments, facilitating your progression within the network. I recommend using a **diagram/map** of the entire environment since otherwise you can get very involved and it is better to work organized, for example Excalidraw.com or Draft.io.

Not having much experience in writing reports, it was not easy and I recommend practicing beforehand. I received the positive result after just 24 hours, unlike what you read online of 15/25 working days.

Here are some **tips** and **insights** to aid your **preparation**:

1. **Thoroughly Review the Letter of Engagement**: Pay close attention to the “Letter of Engagement” document as it provides insights into the exam’s structure and requirements. This document must be included in your final report, along with a graphical representation of the compromised areas marked in red.
2. **It’s Not a CTF**: Unlike traditional Capture The Flag (CTF) challenges, the eCPPTv2 exam is designed to be more approachable.
3. **Master Metasploit**: Proficiency in utilizing Metasploit is paramount, as a good portion of the exam necessitates its usage.
4. **Emphasize Post-Exploitation Techniques**: Effective post-exploitation strategies are crucial for gathering information and pivoting to other machines.
5. **Mind Your Nmap Switches**: Be cautious when using Nmap with non-aggressive settings. Setting it to -T1 can prevent accidental resets and loss of progress during scanning or pivoting.
6. **Patience is Key**: Don’t be discouraged if it takes the full 7 days to compromise the environment. Persistence pays off in the long run.
7. **Act like you’re a journalist:** Take as many screens as possible during the 7 days of access to the lab, or if possible start filling out the report at the same time, because if you forgot to track something, it would be a problem.

Creating a customized **homemade lab**, composed of three or more **network interfaces** is the best training for this exam, starting with network of 2/3 interfaces and machines without vulnerabilities (direct access with SSH for example, [see here](https://app.gitbook.com/o/s2H3MdEB0Qp2IbE58Gxw/s/otIy5NxxVXxLTnh5crZs/~/changes/56/readme/network-security/2.4-1/2.2-pivoting-1)), increasing the network interfaces with more vulnerable machines (including one vulnerable to BoF, such as [Brainpain](https://app.gitbook.com/o/s2H3MdEB0Qp2IbE58Gxw/s/e4F1pi3gddqrR51EW7bB/brainpain-bof)).

Remember that you already have an OVA machine on your VMWare/VirtualBox running on **Windows 10**, with **ImmunityDebugger** and the **Mona** plugin installed, to be used to test and prepare the shellcode to exploit the BoF-vulnerable software running on one of the machines on the network.

The PowerShell, Wi-Fi Security and Ruby modules are certainly important, but not mandatory for passing the exam.

Personally I didn’t follow the INE course, but I relied on the resources found online that I tried to list on [my github](https://github.com/dev-angelist/eCCPTv2-PTP-Notes).

Here below the **path** I used and which I would recommend to reach a level necessary to pass the exam. 👇

### Background Information

* OpenVPN 🏠 [THM Room](https://tryhackme.com/room/openvpn)
* Linux Fundamentals Module 🏠 [THM Room](https://tryhackme.com/module/linux-fundamentals)
* Windows Fundamentals Module 🏠 [THM Room](https://tryhackme.com/module/windows-fundamentals)
* What is Networking 🏠 [THM Room](https://tryhackme.com/room/whatisnetworking)
* Intro To Networking 🏠 [THM Room](https://tryhackme.com/room/introtonetworking)
* Intro To LAN 🏠 [THM Room](https://tryhackme.com/room/introtolan)
* HTTP in Detail 🏠 [THM Room](https://tryhackme.com/room/httpindetail)
* DNS in Detail 🏠 [THM Room](https://tryhackme.com/room/dnsindetail)
* Intro To Offensive Security 🏠 [THM Room](https://tryhackme.com/room/introtooffensivesecurity)
* Pentesting Fundamentals 🏠 [THM Room](https://tryhackme.com/room/pentestingfundamentals)
* Passive Recon 🏠 [THM Room](https://tryhackme.com/room/passiverecon)
* Intro to Research 🏠 [THM Room](https://tryhackme.com/room/introtoresearch)
* Google Dorking 🏠 [THM Room](https://tryhackme.com/room/googledorking)
* Python Basics (_to understand the working of exploit_) 🏠 [THM Room](https://tryhackme.com/room/pythonbasics)
* Active Recon 🏠 [THM Room](https://tryhackme.com/room/activerecon)
* Vulnerabilities 101 🏠 [THM Room](https://tryhackme.com/room/vulnerabilities101)
* Reverse Shell & Bind Shell 🗒️ [Hacking Tutorials Article](https://www.hackingtutorials.org/networking/hacking-netcat-part-2-bind-reverse-shells/)
* eJPTv2 Ine Full Course 🗒️ [eJPTv2 Notes](https://app.gitbook.com/o/s2H3MdEB0Qp2IbE58Gxw/s/PNcjhcAuvH4mlZKYrNu3/)
* ⏩ [Linux Course](https://www.youtube.com/watch?v=qcX89gkdlYs\&list=PLKZZXjqZrqQvfAhgY7Nit5ynpK3kN_3tx) (Italian)🤌 🇮🇹
* ⏩ [Ethical Hacking Course](https://www.youtube.com/watch?v=L90xYiqqjBI\&list=PLKZZXjqZrqQtKGgJuAYhzYczf1KIdswvO\&pp=iAQB) (Italian)🤌 🇮🇹

### Tooling

* BurpSuite: The Basics 🏠 [THM Room](https://tryhackme.com/room/burpsuitebasics)
* BurpSuite: Repeater 🏠 [THM Room](https://tryhackme.com/room/burpsuiterepeater)
* Hydra 🏠 [THM Room](https://tryhackme.com/room/hydra)
* Nmap 🏠 [THM Room](https://tryhackme.com/room/rpnmap)
* Nmap Live Host Discovery 🏠 [THM Room](https://tryhackme.com/room/nmap01)
* Metasploit: Introduction 🏠 [THM Room](https://tryhackme.com/room/metasploitintro)
* Metasploit 🏠 [THM Room](https://tryhackme.com/room/metasploitintro)
* More Detailed Tutorial of Metasploit 🗒️ [NoobLinux Article](https://nooblinux.com/metasploit-tutorial/)
* Nessus 🏠 [THM Room](https://tryhackme.com/room/rpnessusredux)
* WireShark The Basics 🏠 [THM Room](https://tryhackme.com/room/wiresharkthebasics)
* Tmux 🏠 [THM Room](https://tryhackme.com/room/rptmux)
* TShark 🏠 [THM Room](https://tryhackme.com/room/tshark)
* H4cked 🚩 [THM CTF](https://tryhackme.com/room/h4cked) 🟢 - [My Writeup](https://app.gitbook.com/s/rRWtuMw6xkkeDjZfkcWC/thm/h4cked)
* Smag Grotto 🚩 [THM CTF](https://tryhackme.com/room/smaggrotto) 🟢 - [My Writeup](https://app.gitbook.com/s/rRWtuMw6xkkeDjZfkcWC/thm/smag-grotto)
* Lazy Admin 🚩 [THM CTF](https://tryhackme.com/room/lazyadmin) 🟢 - [My Writeup](https://app.gitbook.com/s/rRWtuMw6xkkeDjZfkcWC/thm/lazyadmin)
* Carnage 🚩 [THM CTF](https://tryhackme.com/room/c2carnage) 🟠 - My Writeup
* Warzone 1 🚩 [THM CTF ](https://tryhackme.com/room/warzoneone)🟠 - My Writeup
* Mr Robot CTF 🚩 [THM CTF ](https://tryhackme.com/room/mrrobot)🟠 - My Writeup
* Anonymous 🚩 [THM CTF ](https://tryhackme.com/room/anonymous)🟠 - My Writeup
* Misguided Ghost 🚩 [THM CTF ](https://tryhackme.com/room/misguidedghosts)🔴 - My Writeup

### Web

* OWASP top 10 🏠 [THM Room](https://tryhackme.com/room/owasptop10)
* Inclusion 🏠 [THM Room](https://tryhackme.com/room/inclusion)
* Injection 🏠 [THM Room](https://tryhackme.com/room/injection)
* Web Application Security 🏠 [THM Room](https://tryhackme.com/room/introwebapplicationsecurity)
* Overpass2 🚩 [THM CTF](https://tryhackme.com/room/overpass2hacked) 🟢 - My Writeup
* Vulnversity 🚩 [THM CTF](https://tryhackme.com/room/vulnversity) 🟢 - [My Writeup](https://app.gitbook.com/s/rRWtuMw6xkkeDjZfkcWC/thm/vulnversity)
* Basic Pentesting 🚩 [THM CTF](https://tryhackme.com/room/basicpentestingjt) 🟢
* StartUp 🚩 [THM CTF](https://tryhackme.com/room/startup) 🟢 - [My Writeup](https://app.gitbook.com/s/rRWtuMw6xkkeDjZfkcWC/thm/startup)
* All In One 🚩 [THM CTF](https://tryhackme.com/room/allinonemj) 🟠 - My Writeup
* Daily Bugle 🚩 [THM CTF](https://tryhackme.com/room/dailybugle) 🔴 - My Writeup

### [Buffer Overflow](https://github.com/sidneysimas/eCPPTv2-PTP-Notes/blob/main/readme/system-security/1.3-buffer-overflow.md)

* INE eCPPT BoF Material 🗒️
* TCM BoF [Material ](https://youtu.be/ncBblM920jw?si=qQXZmm2hKh32q9rY)🗒️
* Post Exploitation Basics 🏠 [THM Room](https://tryhackme.com/room/postexploit)
* Sudo Buffer Overflow 🏠 [THM Room](https://tryhackme.com/room/sudovulnsbof)
* Tiberius Buffer Overflow Prep Room🏠 [THM Room](https://tryhackme.com/room/bufferoverflowprep)
* Brainstorm 🏠 [THM Room](https://tryhackme.com/room/brainstorm)
* Gatekeeper 🚩 [THM CTF ](https://tryhackme.com/room/gatekeeper)🟠 - My Writeup
* Brainpan 1 🚩 [THM CTF](https://tryhackme.com/room/brainpan) 🔴 - [My Writeup](https://app.gitbook.com/s/rRWtuMw6xkkeDjZfkcWC/vulnhub/brainpain-bof)
* 🗒️ [https://github.com/Tib3rius/Pentest-Cheatsheets/blob/master/exploits/buffer-overflows.rst](https://github.com/Tib3rius/Pentest-Cheatsheets/blob/master/exploits/buffer-overflows.rsthttps://github.com/gh0x0st/Buffer_Overflowhttps:/boschko.ca/braindead-buffer-overflow-guide-to-pass-the-oscp-blindfolded/)
* 🗒️ [https://github.com/gh0x0st/Buffer\_Overflow](https://github.com/Tib3rius/Pentest-Cheatsheets/blob/master/exploits/buffer-overflows.rsthttps://github.com/gh0x0st/Buffer_Overflowhttps:/boschko.ca/braindead-buffer-overflow-guide-to-pass-the-oscp-blindfolded/)
* 🗒️ [https://boschko.ca/braindead-buffer-overflow-guide-to-pass-the-oscp-blindfolded/](https://github.com/Tib3rius/Pentest-Cheatsheets/blob/master/exploits/buffer-overflows.rsthttps://github.com/gh0x0st/Buffer_Overflowhttps:/boschko.ca/braindead-buffer-overflow-guide-to-pass-the-oscp-blindfolded/)

### Post Exploitation

* Windows Privilege Escalation - [Notes](https://dev-angelist.gitbook.io/windows-privilege-escalation/)
* Post Exploitation Basics 🏠 [THM Room](https://tryhackme.com/room/postexploit)
* Sudo Security Bypass 🏠 [THM Room](https://tryhackme.com/room/sudovulnsbypass)
* Sudo Buffer Overflow 🏠 [THM Room](https://tryhackme.com/room/sudovulnsbof)
* Windows Privilege Escalation 🗒️ [Hackersploit Article](https://hackersploit.org/windows-privilege-escalation-fundamentals/)
* Windows Privesc Arena 🏠 [THM Room](https://tryhackme.com/room/windowsprivescarena)
* Linux Privesc Arena 🏠 [THM Room](https://tryhackme.com/room/linuxprivescarena)
* Windows Privesc 🏠 [THM Room](https://tryhackme.com/room/windows10privesc)
* Bypass UAC 🏠 [THM Room](https://tryhackme.com/room/bypassinguac)
* ⏩ [MsfVenom Guide](https://www.youtube.com/watch?v=XLWyjN_eBhw) (Spanish) 🇪🇸
* Simple CTF 🚩 [THM CTF](https://tryhackme.com/room/easyctf) 🟢 - [My Writeup](https://app.gitbook.com/s/rRWtuMw6xkkeDjZfkcWC/thm/simple-ctf)
* Blaster 🚩 [THM CTF](https://tryhackme.com/room/blaster) 🟢 - [My Writeup](https://app.gitbook.com/s/rRWtuMw6xkkeDjZfkcWC/thm/blaster)
* Blue 🚩 [THM CTF](https://tryhackme.com/room/blue) 🟢 - [My Writeup](https://app.gitbook.com/s/rRWtuMw6xkkeDjZfkcWC/thm/eternal-blue)
* Bounty Hacker 🚩 [THM CTF](https://tryhackme.com/room/cowboyhacker) 🟢 - [My Writeup](https://app.gitbook.com/s/rRWtuMw6xkkeDjZfkcWC/thm/bounty-hacker)
* Ignite 🚩 [THM CTF](https://tryhackme.com/room/ignite) 🟢 - [My Writeup](https://app.gitbook.com/s/rRWtuMw6xkkeDjZfkcWC/thm/ignite)
* Kenobi 🚩 [THM CTF](https://tryhackme.com/room/kenobi) 🟢 - [My Writeup](https://app.gitbook.com/s/rRWtuMw6xkkeDjZfkcWC/thm/kenobi)
* Capture the flag 🚩 [THM CTF](https://tryhackme.com/room/c4ptur3th3fl4g) 🟢 - My Writeup
* Pickle Rick 🚩 [THM CTF](https://tryhackme.com/room/picklerick) 🟢 - [My Writeup](https://app.gitbook.com/s/rRWtuMw6xkkeDjZfkcWC/thm/pickle-rick)
* Empline 🚩 [THM CTF](https://tryhackme.com/room/empline) 🟠 - My Writeup
* Internal 🚩 [THM CTF](https://tryhackme.com/room/internal) 🔴 - My Writeup

### [**Pivoting**](https://github.com/sidneysimas/eCPPTv2-PTP-Notes/blob/main/readme/network-security/2.4-1/2.2-pivoting.md)

* INE eCPPT Pivoting Material 🗒️
* Pivoting using Metasploit 🗒️ [TutorialsPoint Article](https://www.tutorialspoint.com/metasploit/metasploit_pivoting.htm)
* ContainMe 🚩 [THM CTF](https://tryhackme.com/room/containme1) 🟢 - My Writeup
* Wreath 🏠 [THM Room](https://tryhackme.com/r/room/wreath) - [Writeup](https://pencer.io/ctf/ctf-thm-wreath/)
* 🗒️ [https://www.offsec.com/metasploit-unleashed/pivoting/](https://www.offsec.com/metasploit-unleashed/pivoting/)
* 🗒️ [https://pentest.blog/explore-hidden-networks-with-double-pivoting/](https://pentest.blog/explore-hidden-networks-with-double-pivoting/)
* ⏩ [Home Lab: ProxyChains - eCPPT prep](https://www.youtube.com/watch?v=QNoIX1au_CM)
* ⏩ [Pivoting with Ligolo](https://www.youtube.com/watch?v=DM1B8S80EvQ)
* ⏩ [Pivoting with Metasploit ](https://www.youtube.com/watch?v=RotyKByc8Jc)(Spanish) 🇪🇸
* ⏩ [Manual Pivoting using Chisel and Socat](https://www.youtube.com/watch?v=l3IEnXYVjWw\&t=664s) (Spanish) 🇪🇸
* ⏩ [Double Pivoting](https://www.youtube.com/watch?v=zGm7kUvC31M\&t=542s) (Spanish) 🇪🇸
* ⏩ [Pivoting Manual Playlist S4vitar](https://www.youtube.com/watch?v=L1jSoCcvRY4\&t=6380s) (Spanish) 🇪🇸

### Red Team & Active Directory (only for v3)

* [CRTP Notes](https://dev-angelist.gitbook.io/crtp-notes) 🗒️
* [Windows Privilege Escalation - Video EN](https://www.youtube.com/watch?v=n382EGuJP8Y\&list=PLJnLaWkc9xRh8hmNFWyzWMFgAHo8Lgr93) 🇬🇧 🎦
* [OSCP Guide 10/12 – Active Directory - Video EN](https://www.youtube.com/watch?v=26M3POQ_51A\&list=PLJnLaWkc9xRgOyupMhNiVFfgvxseWDH5x\&index=10) 🇬🇧 🎦
* [The Cyber Mentor (TCM) - Hacking Active Directory for Beginners - Video EN](https://www.youtube.com/watch?v=VXxH4n684HE) 🇬🇧 🎦
* [The Cyber Mentor (TCM) - Windows Privilege Escalation for Beginners - Video EN](https://www.youtube.com/watch?v=uTcrbNBcoxQ) 🇬🇧 🎦
* [Cisco and Pentester Academy Attacking Active Directory Class with Nikhil Mittal - Video EN](https://www.youtube.com/watch?v=1fiZbYhEkYA) 🇬🇧 🎦
* [Active Directory - John Hammond Series - Video EN](https://www.youtube.com/watch?v=pKtDQtsubio\&list=PL1H1sBF1VAKVoU6Q2u7BBGPsnkn-rajlp) 🇬🇧 🎦
* [Active Directory THM Room Walkthrough - Esadecimale - Video ITA](https://youtu.be/WEXpcDg25QM?si=XFA4hFbvwxyLSae7) 🇮🇹 🎦

### [**Reporting**](https://github.com/sidneysimas/eCPPTv2-PTP-Notes/blob/main/readme/metasploit-and-ruby-1) **(only for v2)**

It's a good choice use one of these source: **TCM's** template, **Offensive Security's** pentest report, the **ITProTv** sample report, and INE's reporting guide.

* 🗒️[How to write a PT Report — My Notes](https://dev-angelist.gitbook.io/eccptv2-ptp-notes/readme/metasploit-and-ruby-1/7.1)
* ⏩ [Writing a PT Report — TCM](https://www.youtube.com/watch?v=EOoBAq6z4Zk\&t=102s)
* ⏩ [ITProTV Report](https://www.youtube.com/watch?v=NEz4SfjjwvU\&list=WL\&index=11)
* ⏩ [OSCP — How to Take Effective Notes](https://www.youtube.com/watch?v=yYmDQY1zKKE)
* ⏩ [OSCP — How to Write a Report](https://www.youtube.com/watch?v=Ohm0LhFFwVA)

### Other Resources

* eCPPT Field Manual: [https://drive.google.com/file/d/1wC7RMTrWjt74rO8u4X-zM89T\_hZzF\_A5/edit](https://drive.google.com/file/d/1wC7RMTrWjt74rO8u4X-zM89T_hZzF_A5/edit)
* [https://www.hackingarticles.in/lateral-movement-pass-the-hash-attack/](https://www.hackingarticles.in/lateral-movement-pass-the-hash-attack/)
* [https://www.sans.org/posters/pivot-cheat-sheet/](https://www.sans.org/posters/pivot-cheat-sheet/)
* [https://medium.com/@dev-angelist/learning-path-my-experience-for-the-eccptv2-ptp-certification-april-2024-15ddf6b29a8f](https://medium.com/@dev-angelist/learning-path-my-experience-for-the-eccptv2-ptp-certification-april-2024-15ddf6b29a8f)

### CheatSheet <a href="#user-content-e940" id="user-content-e940"></a>

* 🗒️ [eCPPT — CheatSheet](https://app.gitbook.com/o/s2H3MdEB0Qp2IbE58Gxw/s/otIy5NxxVXxLTnh5crZs/~/changes/56/eccpt-cheat-sheet)
* 🗒️ [Windows Privilege Escalation Cheatsheet](https://dev-angelist.gitbook.io/windows-privilege-escalation/cheatsheet)
* 🗒️ [CRTP (Active Directory Notes) Cheatsheet](https://dev-angelist.gitbook.io/crtp-notes/crtp-cheat-sheet)
