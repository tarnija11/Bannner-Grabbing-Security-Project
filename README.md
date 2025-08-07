### Banner Grabbing & Digital Footprinting Countermeasures

This repository documents a comprehensive security project focused on the reconnaissance technique of **banner grabbing** and the implementation of effective **countermeasures** to protect web servers from information leakage. The project's output is a detailed report, which is linked below.

***

### Project Summary

This project addresses the critical security risk posed by default web server banners, which often reveal sensitive details like server software type, version numbers, and operating system information. This metadata can be easily collected by attackers and used to identify known vulnerabilities (CVEs), significantly simplifying the planning of targeted exploits. The project was executed in two phases: first, demonstrating the technique of banner grabbing using common command-line tools, and second, implementing and verifying security countermeasures to minimize information exposure. Our methodology uses a practical lab setup with a macOS machine as the attacking client and a Windows MERN stack server as the target.

***

### Learning Objectives

* **Understanding Banner Grabbing:** Grasp the mechanics of how banner grabbing works and the specific types of information it reveals.
* **Vulnerability Assessment:** Learn how to correlate banner information with public vulnerability databases to identify potential attack vectors.
* **Defensive Strategies:** Gain hands-on experience implementing server-side configuration changes to suppress or alter banners, thereby enhancing security.
* **Responsible Disclosure:** Practice ethical hacking principles by demonstrating responsible information gathering and advocating for secure server configurations.

***

### Implementation & Infrastructure

This project leverages a client-server architecture using a real-world setup. The "attack" phase uses standard network tools on a Mac to probe a Windows-based MERN server. The "defense" phase involves modifying configuration files on the Windows server to obscure or remove the banner information.

**Attacking Machine (macOS):**
* **Tools:** `telnet`, `curl`, and `nmap` were used to perform various types of banner grabbing, from simple connections to detailed service version scans.

**Target Web Server (Windows MERN Stack):**
* **Platform:** A Windows machine hosting a MERN (MongoDB, Express, React, Node.js) application.
* **Countermeasures:** Configurations were modified on the web server (e.g., Apache or Nginx) to disable `ServerSignature` and `ServerTokens`, as well as on the Express.js application to remove the `X-Powered-By` header.

***

###  Full Project Report

For a complete breakdown of the project, including step-by-step commands, conceptual screenshots, and a detailed analysis of the findings and recommendations, please see the full report below.

**[➡️ Project Report: https://docs.google.com/document/d/1FVJA9H-8kwo9ezbDnFpI4MUQDnLKP2kqS-l3hdt2zBQ/edit?usp=sharing]((https://docs.google.com/document/d/1FVJA9H-8kwo9ezbDnFpI4MUQDnLKP2kqS-l3hdt2zBQ/edit?usp=sharing))**
