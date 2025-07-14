# Snoopy Server System Setup

This repository contains the automated system configuration for the **Snoopy server**, designed for **lab and testing purposes**. 

It uses **Ansible** to provision the entire server stack: networking, monitoring, containerization, GNS3 lab environment, and more, all in a **consistent and reproducible** way.

## Purpose

Quickly bring a new Snoopy server into a ready-to-use state.  
Automate the installation of all required software and services.  
Save time and reduce human error when setting up lab and testing environments.  
Integrate with GitHub Actions for CI/CD and secrets management.

## What it configures

The Ansible playbook provisions the following components on the server:

- Base OS hardening and setup (locale, SSH, updates)
- Networking: loopback and TAP interfaces for lab networks, static IP configuration
- GitHub Actions Runner: registers the server as a self-hosted runner with your repo
- Docker: installs and configures Docker for containers
- QEMU: sets up QEMU for VM testing
- GNS3: installs GNS3 server and dependencies, syncs lab data from Mega cloud storage
- Certbot: LetsEncrypt client for SSL certificates
- Traefik: reverse proxy with dashboard and HTTPS support
- Netdata: real-time monitoring and metrics dashboard
