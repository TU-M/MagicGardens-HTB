# MagicGardens Exploitation Report

## Overview
This report details the exploitation of the MagicGardens machine, highlighting various attack vectors including web application vulnerabilities, network exploitation, Docker security weaknesses, and privilege escalation techniques.

## Steps of Exploitation

### 1. Exploiting the Django Website
- Tricked the website into approving a premium subscription purchase.
- Injected a **Cross-Site Scripting (XSS)** payload into a QR code.
- Captured the admin’s authentication cookie.

### 2. Accessing the Django Admin Panel
- Used the stolen admin cookie to gain **Django admin panel** access.
- Retrieved a **hash and SSH credentials**.

### 3. Exploiting Network Monitoring Software
- Identified a buffer overflow vulnerability in the **IPv6 handler** of a custom network monitoring tool.
- Exploited it to obtain a shell as another user.

### 4. Accessing the Docker Registry
- Discovered that the compromised user had access to the **Docker Registry**.
- Found the container image for the Django website.
- Extracted a **hardcoded secret** from the image.

### 5. Exploiting Deserialization Vulnerability
- Leveraged a **deserialization vulnerability** in the container.
- Gained a **root shell** inside the container.

### 6. Privilege Escalation to Root
- Used the ability to **load kernel modules** inside the container.
- Escalated privileges to gain **root access on the host machine**.

## Conclusion
Through a series of vulnerabilities, I successfully obtained **full control over the MagicGardens machine**. This attack chain demonstrates the importance of **secure authentication, network protection, Docker security, and kernel module restrictions**.

## Disclaimer
This report is for **educational and ethical hacking purposes only**. Unauthorized access to systems without proper authorization is illegal.
