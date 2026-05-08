# Home Server Setup & Ubuntu Server Deployment
## Overview

This project documents the setup and deployment of a self-hosted Ubuntu Server environment on a dedicated desktop machine.

The goal of this setup is to create a stable and scalable home server infrastructure for:

 - Python automation
 - Telegram bots
 - Web dashboards
 - Monitoring systems
 - Self-hosted services
 - Future AI agent and cybersecurity experiments

# Hardware Setup
## Server Hardware
 - Desktop PC
 - 256GB SSD
 - LAN network deployment
 - Headless operation (SSH-only after deployment)

# Operating System
Ubuntu Server 24.04 LTS

Reasons for choosing Ubuntu Server:

 - Long-term support (LTS)
 - Stability
 - Lightweight
 - Excellent compatibility with Python, Docker, and automation tools

# Initial Server Configuration
## Features Configured
 - Static IP address
 - SSH remote access
 - UFW firewall
 - Python virtual environment
 - Supervisor process management
 - Docker installation
 - Uptime Kuma monitoring

# Networking
## Static IP Configuration

Configured using Netplan:

 - Static IP assignment
 - Gateway routing
 - DNS configuration

Challenges encountered during setup:

 - Subnet mismatch
 - Gateway routing issue
 - DNS resolution issue

These were resolved through manual Netplan configuration and route validation.

# Python Automation Environment

Created an isolated Python environment using:

 - python3-venv
 - pip
 - virtual environments

This allows clean dependency management for multiple automation projects.

# Telegram Forwarder Bot Deployment

A Telegram forwarding bot was deployed on the server.

## Features
 - Web dashboard
 - Telegram integration
 - Async bot architecture
 - FastAPI web interface

# Architecture Refactor

The original implementation ran both:

 - Telegram bot
 - FastAPI web server

inside a single process.

This caused asyncio event loop conflicts and web request hanging.

The system was refactored into:

 - bot_main.py
 - web_main.py

running as independent processes.

# Process Management
## Supervisor

Supervisor was used for:

 - Auto-start on boot
 - Automatic restart on crash
 - Process monitoring
 - Persistent background execution

Configured services:

 - telefeed-bot
 - telefeed-web

# Monitoring System
## Uptime Kuma

Installed using Docker.

Used for:

 - Web dashboard uptime monitoring
 - Heartbeat monitoring
 - Telegram alerts
 - Service health monitoring

# Skills Demonstrated
 - Linux server administration
 - SSH remote management
 - Networking & static IP configuration
 - Firewall management
 - Python deployment
 - FastAPI deployment
 - Async architecture troubleshooting
 - Docker container deployment
 - Monitoring & alerting
 - Process supervision
 - Production debugging

# Future Improvements

Planned upgrades:

 - Nginx reverse proxy
 - HTTPS / SSL
 - Domain integration
 - Centralized logging
 - Multi-service orchestration
 - AI-assisted monitoring
 - Automated deployment pipeline
 - conversion of partial 500gb existing HDD disk to Linux storage

# Technologies Used
 - Ubuntu Server 24.04 LTS
 - Python
 - FastAPI
 - Uvicorn
 - Supervisor
 - Docker
 - Uptime Kuma
 - SSH
 - UFW Firewall
 - Netplan

## Author
Kamarul Nizam
