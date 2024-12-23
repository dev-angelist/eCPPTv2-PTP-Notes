# 1️⃣ 1 - ​System Security

### Topics

> 1. [Architecture Foundamentals](broken-reference)
> 2. [Assemblers and Tools](broken-reference)
> 3. [Buffer Overflow](broken-reference)
> 4. [Cryptography](broken-reference)
> 5. [Malware](broken-reference)
> 6. [Shellcoding](broken-reference)

> #### ❗ Disclaimer
>
> **Never use tools and techniques on real IP addresses, hosts or networks without proper     authorization!**
>
> ❗_**Never run these techniques on un-authorized addresses**_

## What is a Binary Exploitation?

<details>

<summary>What is a Binary Exploitation?</summary>

**Binary exploitation** refers to the process of taking advantage of vulnerabilities in binary code, typically executable files, to gain unauthorized access, control, or manipulate a computer system. Binary exploitation is a common technique employed in the field of cybersecurity, particularly in the realm of offensive security and penetration testing.

Here's a breakdown of key concepts related to binary exploitation:

1. **Binary Code:** Computers execute instructions in the form of binary code, which consists of sequences of 0s and 1s. Executable files, such as those with extensions like .exe or .elf, contain binary code that the computer's processor can execute.
2. **Vulnerabilities:** Binary exploitation often involves identifying and exploiting vulnerabilities in software. These vulnerabilities can range from buffer overflows and format string vulnerabilities to insecure input handling or poor memory management.
3. **Exploits:** An exploit is a piece of code or a series of commands that takes advantage of a specific vulnerability to compromise a system's security. Exploits are crafted to manipulate the binary code in a way that allows an attacker to achieve their objectives, such as gaining unauthorized access or executing arbitrary code.
4. **Buffer Overflow:** One common type of vulnerability is a buffer overflow, where an attacker overflows a program's buffer to overwrite adjacent memory, potentially leading to the execution of malicious code.
5. **Shellcode:** In binary exploitation, shellcode is a small piece of code that is often injected into a vulnerable program to spawn a shell. This shell provides the attacker with a command-line interface and control over the compromised system.
6. **ROP (Return-Oriented Programming):** ROP is a technique used in binary exploitation where the attacker combines short sequences of existing code (gadgets) to perform specific actions without injecting new code. This is often used to bypass security mechanisms like Data Execution Prevention (DEP).

Binary exploitation is a skill often honed by security professionals and ethical hackers to identify and address security weaknesses in software. However, it can also be misused by malicious actors for unauthorized access and attacks. It's crucial for software developers to be aware of secure coding practices to minimize the risk of vulnerabilities in their applications.

</details>

## Other Resources

{% embed url="https://www.ired.team/offensive-security/code-injection-process-injection/binary-exploitation" %}

* [KNX - Binary Exploitation v1 YT PlayList 🇮🇹](https://www.youtube.com/watch?v=3a_1zIMKMtE\&list=PLimbw9yhOVDYOJ-1wTlR4Jjxcsr4EuZa2)
* [KNX - Binary Exploitation v2 YT PlayList 🇮🇹](https://www.youtube.com/watch?v=tZsjIUkrcB8\&list=PLimbw9yhOVDZbmYKhKOF4JR9OQbWfvFdi)
* [TCM - Buffer Overflows YT](https://www.youtube.com/watch?v=ncBblM920jw) 🇬🇧
* [Kevin Du - BoF YT PlayList](https://www.youtube.com/watch?v=LBo56Xyowvk\&list=PLW56THlev-gAhS9g1HdZn9TcQo3Hm-kgf) 🇬🇧
* [LiveOverflow - Binary Exploitation YT PlayList ](https://www.youtube.com/watch?v=iyAyN3GFM7A\&list=PLhixgUqwRTjxglIswKp9mpkfPNfHkzyeN)🇬🇧
