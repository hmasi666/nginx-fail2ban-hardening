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

## Security Approach

This project is based on a practical layered hardening model for a self-hosted Linux web service.

The main idea is:

- reduce exposure with Nginx hardening
- detect malicious requests from logs
- automatically ban abusive IP addresses with Fail2ban
- document reusable filters and jail configurations

Instead of relying only on default protections, this setup also includes custom filters for suspicious scan patterns and web attack behavior.

Examples of targeted activity include:

- SSH brute force attempts
- repeated HTTP authentication failures
- automated bot scanning for common admin paths
- vulnerability probes targeting known web application files
- traversal-style requests and suspicious execution attempts

The goal is not to eliminate all risk, but to reduce noisy attack traffic, improve visibility, and create a maintainable baseline for a hardened public-facing service.

## Repository Structure

- `fail2ban/jail.d/` – example jail configurations
- `fail2ban/filter.d/` – custom Fail2ban filters
- `nginx/snippets/` – example Nginx hardening snippets
- `docs/` – project notes and supporting documentation

- ## Next Steps

Possible future additions to this repository:

- more custom Fail2ban filters
- example jail tuning for different environments
- additional Nginx hardening patterns
- deployment notes for Flask/uWSGI-based services
- example log samples for testing filters
