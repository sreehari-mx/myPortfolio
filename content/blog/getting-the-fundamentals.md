---
title: "Getting The Fundamentals"
description: "This post shares my past couple of month's learning experiences as a beginner in cybersecurity."
date: 2025-07-27
draft: false
weight: 101
cover:
    image: "/blog/getting-the-fundamentals/getting-the-fundamentals-cover.png"
---
# From Packets to Protocols: My Cybersecurity Learning Journey as a Beginner

## Introduction

In this post, I’d like to share my learning journey over the past couple of months as a beginner in cybersecurity. I started with the basics of computer networking, explored key protocols, practiced Linux fundamentals, and even dipped my toes into programming. If you're also just starting out in this exciting field, I hope this post will offer some guidance, inspiration, or simply reassurance that you’re not alone.

---

## Networking: The Foundation of Cybersecurity

- When I first began exploring cybersecurity, I quickly realized that **networking is the foundation** of everything. Over the past few months, I’ve been learning, experimenting, and practicing the core concepts behind how data moves across the internet and internal networks.

- I was already using **Ubuntu on VMware** for some light programming and experimentation. So I had a basic understanding of Linux commands. However, I had *zero knowledge of networking*, especially since I don’t come from a computer science background.

- I started searching for **“Networking for Beginners”** on YouTube. I watched tons of videos—some more helpful than others. **David Bombal’s CCNA playlist** was a standout. It gave me a clear understanding of network devices and how they function.

- But I wanted more depth, so I searched for full beginner networking courses and found a **12-hour video course**(You can find the link in the Resources section.). It wasn’t the most viewed, but it clearly explained concepts like the **TCP/IP model (layer by layer), switches, routers, subnetting**, and essential terminology. I completed it in a week.

- One mistake I made early on was **not taking structured notes**. I watched the videos and understood the concepts, but most of the information faded after a few weeks. That’s when I decided to keep a dedicated **Cybersecurity Notebook**—a game-changer.

- I soon realized theory wasn’t enough. I needed **hands-on practice**. So I installed **Cisco Packet Tracer** on Ubuntu and began creating simple networks by following YouTube tutorials. This was a turning point—it helped me visualize and *truly understand how data flows* through a network. I simulated **ARP, ICMP, STP** traffic and observed how different protocols work.

- **Jeremy’s CCNA playlist** helped me with creating subnets and configuring switches and routers via CLI.

- As my curiosity grew, I started asking questions like:
  - *How do these protocols actually work?*
  - *Why are they needed?*
  - *What happens when I tap the “Wi-Fi” button on my smartphone?*

  I used **ChatGPT** to get answers, and that curiosity kept fueling my progress.

- After gaining confidence with simulations, I moved on to capturing **real network traffic** using **Wireshark**. I set up a **Kali Linux VM** and captured traffic during activities like:
  - Downloading files
  - Running `apt update`
  - Streaming YouTube videos
  - Sending HTTP/HTTPS/FTP/DNS requests
  - Connecting via VPNs

- I experimented with **network interfaces, tunneling, and gateways**, and also explored tools like **Tor, VPNs, and proxychains**.

---

## Google Cybersecurity Certificate

I completed the **Google Cybersecurity Professional Certificate** on Coursera in about a month. It’s a beginner-friendly, theory-heavy course with practical labs in:

- **Linux Fundamentals**: File structure, permissions, user management, etc.
- **SQL Basics**: Filtering and analyzing data from log files.
- **Python Scripting**: Automating tasks like parsing logs.
- **SIEM Tools**: Intro to Chronicle, Splunk.
- **IDS Tools**: Suricata, basic packet analysis using Wireshark and tcpdump.

It also covered essential cybersecurity concepts like:

- **Risk assessment, threat modeling, vulnerabilities**
- **MITRE ATT&CK, NIST RMF frameworks**
- **Incident response, detection and recovery workflows**
- **Job preparation**: Resume tips, interview prep, and how to use AI tools in job searching.

One of the most motivating parts of the course was hearing real-life stories from **Google cybersecurity professionals who came from non-CS backgrounds**. It reassured me that a non-traditional path into cybersecurity is not only possible but increasingly common.

---

## Linux & Virtual Labs

After completing the Google course, I focused on **Linux and building virtual labs** using VMware. I installed **Kali Linux, Debian**, and **Metasploitable2** in an isolated virtual environment to practice safely.

### Key Tools & Skills I Focused On:

- **Wireshark**: Captured live traffic and studied TCP/IP behavior (three-way handshake, sequence numbers, acknowledgments, headers, etc.)
- **Nmap**: Explored different scan types, observed traffic patterns during scans, and captured packets to understand what's happening behind each command.
- **UFW Firewall**: Installed on Debian, tested different configurations, and observed how firewall rules affect Nmap scans.
- **Apache2 Setup**: Hosted a basic site on Debian, accessed it from Kali, and captured HTTP request/response headers.
- **Password Cracking**: Used **John the Ripper** for encryption, decryption, and hash cracking practice.

---

### Attacking Vulnerable Machines (Ethically)

After getting familiar with tools and basic protocols, I began exploring **vulnerable machines** (for ethical hacking practice).

#### 🛡️ Attack 1: ARP Spoofing with Ettercap

- Kali (attacker), Debian (client), Metasploitable2 (server)
- Used **Ettercap** to spoof ARP tables
- Logged into an HTTP service from the client and captured the **username and password** on the attacking machine

#### 🛡️ Attack 2: VSFTPD Exploit

- Used **Metasploit** to exploit the **vsftpd backdoor vulnerability**
- Learned that if a username included `:)`, it triggered a shell on **port 6200**
- Connected manually via **netcat** and obtained a **reverse shell**

#### 🛡️ Attack 3: Brute-Force FTP Login

- Used **Hydra** to perform brute-force attack on FTP credentials
- Captured both network traffic and login attempts via logs

---

## Questions That Drove My Curiosity

Here are some of the key questions that kept me exploring deeper:

- What is the internet, and how does it work?
- What actually happens when we tap the Wi-Fi or network button on a smartphone?
- Can ISPs see everything we search?
- What does "1.5GB/day" actually mean, and how do ISPs enforce it?
- How do VPNs work, and why are they important?
- What are IP addresses, and why do we have both private and public ones?
- How does DNS work?
- What’s the difference between a modem and a router?
- How do devices on a LAN get their IP addresses?
- How does traceroute work?
- What happens when we run `sudo apt update`?
- How does the Linux file permission system work?

---

## Conclusion

When I started learning networking, I had a lot of questions (some of which are listed above). That curiosity became the fuel for my journey. Today, I have a **solid foundational understanding of networking**, protocols, traffic analysis, and basic attack vectors.

I can confidently explain how the internet works, the role of clients and servers, and how different protocols interact at each layer.

This is the **first big step in my cybersecurity journey**, and I'm excited for what’s ahead.

If you’re a beginner like me, I hope this post gave you some insights, motivation, or just reassurance that you’re on the right path. Keep asking questions—and keep learning.

---

## Resources I Used

### Networking

- 🎥 [David Bombal CCNA Playlist](https://youtube.com/playlist?list=PLw6kwOJVj3MbMZ8B72ZgUryj8OSETC0ds&si=RzCeOnXK8xC0yq71)  
- 🎥 [Jeremy’s IT Lab CCNA Playlist](https://youtube.com/playlist?list=PLxbwE86jKRgMpuZuLBivzlM8s2Dk5lXBQ&si=1Jy53l4ldTqdoaOw)  
- 🎥 [Chris Greer Wireshark Tutorials](https://youtube.com/playlist?list=PLW8bTPfXNGdA_TprronpuNh7Ei8imYppX&si=L5M5eU8txD1hxQpS)  
- 📺 [Networking Full Course](https://youtu.be/PhjHXeMNpp8?si=iDle7xkgNZIYN68L)

### Linux Fundamentals

- 🎥 [NetworkChuck - Linux for Hackers](https://youtube.com/playlist?list=PLIhvC56v63IJIujb5cyE13oLuyORZpdkL&si=Os2xPBUmFyXzi-rC)  
- 🕹️ [OverTheWire - Bandit Wargame](https://overthewire.org/wargames/bandit/)  
- 🔐 [TryHackMe - Linux Fundamentals](https://tryhackme.com/)  
- 🎓 [TCM Security - Linux 101: Fundamentals](https://academy.tcm-sec.com/p/linux-fundamentals)  

---

## Thank You 

Thank you for taking the time to read about my journey. If you're just starting out in cybersecurity like I did, I hope this post gave you some direction or motivation. Feel free to connect or reach out if you're on a similar path — I'd love to learn together!

Happy learning, and stay curious!
