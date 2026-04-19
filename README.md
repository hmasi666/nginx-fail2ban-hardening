nginx-fail2ban-hardening

Practical server hardening project for a self-hosted Linux web service using Nginx and Fail2ban.

Overview

This repository documents a real-world server hardening setup used to protect a publicly exposed web service.

The focus is on detecting and blocking malicious traffic using Fail2ban, along with basic Nginx hardening techniques.

Current Setup

The following Fail2ban jails are currently in use:

sshd
nginx-http-auth
nginx-botsearch
nginx-common-attacks
nginx-cve-scan
uwsgi-php-eval

These cover:

SSH brute force attempts
HTTP authentication attacks
automated bot scanning
common web attack patterns
known CVE-related probes
suspicious PHP/uWSGI execution attempts
Goals
Improve real-world server security
Learn how to detect malicious requests in logs
Build custom Fail2ban filters
Document a practical hardening setup for future reuse
Environment
Linux server (Raspberry Pi)
Nginx
Fail2ban
uWSGI / Flask
Notes

This project was developed with the help of AI tools (ChatGPT) for:

idea exploration
debugging
refining configurations

All configurations were tested and adapted manually in a real server environment.

Sensitive information such as real domains, IP addresses, and credentials has been removed from this public version.
