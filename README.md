# Satellite Subscription Management Automation

![Ansible Version](https://img.shields.io/badge/Ansible-2.9+-green.svg)
![RHEL Version](https://img.shields.io/badge/RHEL-8-red.svg)
![License](https://img.shields.io/badge/License-MIT-blue.svg)

A robust Ansible automation solution for managing Red Hat Satellite subscriptions across multiple environments (CNF, Azure, GCP) for Albertsons/Safeway infrastructure.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Directory Structure](#directory-structure)
- [Configuration](#configuration)
- [Usage](#usage)
- [Environment Details](#environment-details)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## 🔍 Overview

This repository contains Ansible playbooks and configuration files for automating the management of Red Hat Satellite subscriptions across different cloud environments. It handles subscription registration, certificate management, and environment-specific configurations for CNF, Azure, and GCP infrastructures.

## ✨ Features

- Automated subscription management for multiple environments
- Environment-specific configuration handling
- Certificate management and renewal
- Robust error handling and retries
- Support for different cloud platforms:
 - CNF (East/West)
 - Azure (East/West US)
 - GCP (US West 2)
- Detailed logging and reporting

## 📝 Prerequisites

- Ansible 2.9 or higher
- RHEL 8.x target systems
- SSH access to target hosts
- Sudo privileges on target hosts
- Valid Red Hat Satellite credentials
- Network access to Satellite servers

## 📁 Directory Structure

├── README.md
├── ansible.cfg
├── inventory/
│   ├── production/
│   │   ├── hosts.yml
│   │   └── group_vars/
│   └── staging/
│       ├── hosts.yml
│       └── group_vars/
├── playbooks/
│   ├── subscription-manager-setup.yml
│   └── roles/
│       └── satellite-subscription/
│           ├── tasks/
│           ├── handlers/
│           └── templates/
└── vars/
├── cnf-west.yml
├── cnf-east.yml
├── azure-west.yml
├── azure-east.yml
└── gcp-west.yml

