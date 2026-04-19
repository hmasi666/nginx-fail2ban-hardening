# Project Notes

## Purpose

This project was created to improve the security of a self-hosted Linux web service exposed to the public internet.

The main purpose was not only to block malicious traffic, but also to better understand what kind of automated scans and attack patterns are commonly visible in real server logs.

## What I learned

During this project I learned more about:

- how Fail2ban works with log-based detection
- how custom filters can be used to catch suspicious request patterns
- how Nginx can be hardened to reduce unnecessary exposure
- how layered protection works in practice on a small public-facing server
- how to document and sanitize a real configuration for public portfolio use

## Practical lessons

One important lesson from this project was that even a small self-hosted service receives a constant stream of unwanted traffic, such as:

- brute force login attempts
- scans for WordPress and phpMyAdmin paths
- probes for exposed configuration files
- requests targeting common web vulnerabilities

This project helped turn those observations into a more structured and reusable security baseline.

## Portfolio note

This repository is based on a real setup adapted into a public example.

AI tools were used during the process for brainstorming, debugging, and documentation support, but the final setup was tested and adjusted manually in a real environment.
