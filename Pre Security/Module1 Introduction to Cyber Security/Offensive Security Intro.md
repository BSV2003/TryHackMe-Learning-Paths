# Offensive Security Intro
Hack your first website (legally in a safe environment) and experience an ethical hacker's job.

## What is Offensive Security?

Offensive Security involves **legally simulating cyber attacks** by exploiting vulnerabilities, misconfigurations, and application flaws to gain unauthorized access **with permission**, in order to improve system defenses.

### Command-line Application
Command-line applications are computer programs designed to be used through a **text-based interface**, without a graphical user interface (GUI).

---

## Gobuster

Gobuster is a **free and open-source directory and file enumeration tool**.  
Penetration testers and security professionals use it to discover **hidden directories and files** on web servers.

### Command Used
```bash
gobuster -u http://fakebank.thm -w wordlist.txt dir
```

#### Command Breakdown
|Flag|  |Description|
|-----------|------|------------------|
|`-u` | URL | Target URL|
|`-w` | Wordlist | Wordlist containing possible directory names|
|`dir` | Mode | Directory brute-forcing mode|

In newer versions of **Gobuster (v3+)**, the mode is typically placed immediately after the main command. The correct modern syntax would be:
```bash
gobuster dir -u http://fakebank.thm -w wordlist.txt
```

### Output
```
=====================================================
Gobuster v2.0.1              OJ Reeves (@TheColonial)
=====================================================
[+] Mode         : dir
[+] Url/Domain   : http://fakebank.thm/
[+] Threads      : 10
[+] Wordlist     : wordlist.txt
[+] Status codes : 200,204,301,302,307,403
[+] Timeout      : 10s
=====================================================
2024/05/21 10:04:38 Starting gobuster
=====================================================
/images (Status: 301)
/bank-transfer (Status: 200)
=====================================================
2024/05/21 10:04:44 Finished
=====================================================
```

- **Status 200** indicates an accessible page
- `/bank-transfer` revealed a sensitive endpoint

---

## Careers in Cyber Security (Offensive Roles)

### 🔴 Penetration Tester
Responsible for testing applications, networks, and systems to identify **exploitable security vulnerabilities**. Penetration testers simulate real-world attacks and report findings so organizations can fix weaknesses before attackers exploit them.

### 🔴 Red Teamer
Acts as a **realistic adversary** by emulating advanced attack techniques against an organization. Red Teamers evaluate the effectiveness of detection, response, and defense mechanisms by thinking and operating like real attackers.

### 🔴 Security Engineer
Designs, implements, monitors, and maintains **security controls, networks, and systems**. Security Engineers help prevent cyberattacks by strengthening infrastructure, improving security architecture, and responding to security risks.
