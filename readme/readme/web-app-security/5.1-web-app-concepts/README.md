# 5.1 - Web App Concepts

## Web Application

#### Topics

> 1. [HTTP/S Protocol Basics](../../../ecpptv3/web-app-security/5.1-web-app-concepts/5.1.1-http-s-protocol.md)
> 2. [Encoding](../../../ecpptv3/web-app-security/5.1-web-app-concepts/5.1.2-encoding.md)
> 3. [Same Origin](../../../ecpptv3/web-app-security/5.1-web-app-concepts/5.1.3-same-origin.md)
> 4. [Cookies](../../../ecpptv3/web-app-security/5.1-web-app-concepts/5.1.3-same-origin.md)
> 5. [Session](../../../ecpptv3/web-app-security/5.1-web-app-concepts/5.1.5-session.md)
> 6. [Web Application Proxies](../../../ecpptv3/web-app-security/5.1-web-app-concepts/5.1.6-web-app-proxies.md)

A **Web Application**, is a computer program or software application that is accessed and interacted with through a web browser over a network, typically the internet. Unlike traditional desktop applications, web apps do not need to be installed on a user's device; instead, users can access them through a web browser.

Web apps can serve a variety of purposes and provide a wide range of functionalities. They can be simple, such as a basic to-do list application, or complex, like a collaborative document editing platform. Common examples of web apps include email services, social media platforms, online banking systems, and productivity tools.

Key characteristics of web apps include:

1. **Accessibility:** Users can access web apps from any device with a compatible web browser and an internet connection, making them platform-independent.
2. **Cross-Platform Compatibility:** Web apps can run on different operating systems, including Windows, macOS, and Linux, as they are not tied to a specific device or OS.
3. **Updates and Maintenance:** Updates and maintenance are centralized on the server, and users do not need to manually update their applications. This allows developers to push updates seamlessly.
4. **No Installation Required:** Users do not need to download or install anything on their devices to use a web app. This reduces the burden on users and eliminates compatibility issues associated with different operating systems.
5. **Collaboration and Sharing:** Web apps often facilitate collaboration and data sharing among users, making them suitable for collaborative work environments.

Web apps are built using various web technologies such as HTML, CSS, and JavaScript. The server-side logic is implemented using programming languages like Python, Ruby, Java, or PHP. Additionally, many modern web apps utilize frameworks and libraries to streamline development and enhance functionality.

### Web Basics

* ​[Web Application Basics](https://attackdefense.com/listing?labtype=webapp-web-app-basics\&subtype=webapp-web-app-basics-getting-started)​
* ​[Web Apps Tools of Trade](https://attackdefense.com/listing?labtype=webapp-tools-of-trade\&subtype=webapp-tools-of-trade-getting-started)

## **Web App Pentesting**

<details>

<summary>Web App Pentesting</summary>

**Web App Pentesting** is a method of evaluating the security of a web application by simulating a cyberattack. The goal of such testing is to identify vulnerabilities and weaknesses within the application that malicious hackers could exploit. By conducting these tests, organizations can proactively strengthen their web applications' security and protect sensitive data.

Key aspects of web application penetration testing include:

1. **Identifying Vulnerabilities:** Penetration testers aim to discover security vulnerabilities, such as code flaws, misconfigurations, and design weaknesses that could be exploited by attackers. Common vulnerabilities include SQL injection, cross-site scripting (XSS), cross-site request forgery (CSRF), and insecure authentication methods.
2. **Mimicking Real Attacks:** Testers simulate real-world attack scenarios to determine how an attacker might compromise the application. This might involve attempting to gain unauthorized access, execute code, or extract sensitive data from the application.
3. **Manual and Automated Testing:** A combination of manual testing by skilled security professionals and automated tools is typically used. Manual testing allows for more comprehensive exploration, while automated tools can efficiently scan for common vulnerabilities.
4. **Exploitation and Verification:** If a vulnerability is identified, the tester may attempt to exploit it to demonstrate its real-world impact. This often involves attempting to escalate privileges or access sensitive data. The success of the exploitation helps confirm the vulnerability's severity.
5. **Reporting:** The results of the penetration test are documented in a comprehensive report, including the identified vulnerabilities, their severity, and recommendations for remediation. This report serves as a roadmap for addressing security issues.
6. **Remediation:** After vulnerabilities are identified, the development and security teams work together to address and fix the issues. This may involve patching code, changing configurations, or implementing new security measures.
7. **Ongoing Testing:** Web application penetration testing is not a one-time effort. Regular testing, especially after significant changes to the application, is crucial to maintaining a strong security posture.

The objectives of web application penetration testing are to:

* Uncover and fix security vulnerabilities before malicious attackers can exploit them.
* Ensure compliance with industry standards and regulations.
* Increase the overall security and trustworthiness of the web application.
* Safeguard sensitive data, user accounts, and user privacy.
* Minimize the risk of security breaches and data leaks.

</details>

### Practise

🔬 There are many vulnerable testing web apps like:

* ​[Juice Shop - Kali Install](https://www.kali.org/tools/juice-shop/)​
* ​[DVWA - Kali Install](https://www.kali.org/tools/dvwa/)​
* ​[bWAPP](http://www.itsecgames.com/)​
* ​[Mutillidae II](https://github.com/webpwnized/mutillidae)

<details>

<summary>DVWA</summary>

**The Damn Vulnerable Web Application (DVWA)** is a web application built with PHP and MySQL intentionally designed to be susceptible to security vulnerabilities. Its primary purpose is to serve as a resource for security professionals to assess their skills and tools within a legal context. Additionally, it aids web developers in gaining a deeper understanding of the processes involved in securing web applications and facilitates learning about web application security for both students and teachers in a controlled classroom setting.

DVWA is designed to provide a platform for practicing various common web vulnerabilities at different difficulty levels, all presented through a simple and user-friendly interface. It's important to note that there are deliberate both documented and undocumented vulnerabilities within the software, encouraging users to explore and identify as many issues as possible.

</details>

{% embed url="https://github.com/digininja/DVWA" %}
DVWA
{% endembed %}

#### Theory and Lab platform

{% embed url="https://portswigger.net/web-security/all-labs" %}
Web Burp Suite Security Academy
{% endembed %}

> #### ❗ Disclaimer
>
> * **Never use tools and techniques on real IP addresses, hosts or networks without proper authorization!**
