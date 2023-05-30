---
title: Basics of SSH Security
description: ssh configuration
published: true
date: 2023-05-30T15:26:40.473Z
tags: ssh, security
editor: markdown
dateCreated: 2023-05-29T13:37:59.559Z
---

\# Basics of SSH security

  
 

\### Here are some basic steps you can take to optimize SSH security:

  
 

\- Change the default SSH port: This can help to reduce the number of automated attacks as attackers are often targeting systems that are running SSH on the default port 22.

  
 

\- Disable SSH root access: This can help to reduce the risk of unauthorized access to your system as attackers often target the root account. Instead, create a separate user with sudo privileges.

  
 

\- Use strong SSH key-based authentication: Use a strong password and consider using public key-based authentication instead of simple password authentication. This provides an extra layer of security in that an attacker would need to possess the private key to gain access, which is much more difficult to obtain than a simple password.

  
 

\- Limit the number of authentication attempts: Use an authentication method that limits the number of failed login attempts, such as fail2ban. This can help prevent brute-force attacks.

  
 

\- Keep software up-to-date: Make sure that both the SSH server and client software is up-to-date and has all security patches applied.

  
 

\### Lets start implementing them:

  
 

\##### Change the default SSH port:

  
 

Open the SSH configuration file using a text editor:

\`\`\`bash

sudo nano /etc/ssh/sshd\_config

\`\`\`

Find the line that says #Port 22 and uncomment it or change the port number to your desired port, \*for example, Port 2222\*.

Save the file and exit.

Restart the SSH service:

\`\`\`bash

sudo service sshd restart.

\`\`\`