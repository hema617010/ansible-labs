# ansib# Ansible Labs Project

This repository contains two Ansible labs demonstrating infrastructure automation, configuration management, and service deployment using best practices.

## Project Structure

lab1/
- inventory
- ansible.cfg
- playbook.yml

lab2/
- site.yml
- inventory
- group_vars/
- roles/
  - iti-webserver-role/
  - jenkins-role/
- mariadb-server/

## Lab 1 – Basic Ansible Automation

- Install and configure Ansible control node
- Set up SSH key-based authentication
- Configure inventory and ansible.cfg with privilege escalation
- Use ad-hoc commands and playbooks
- Create user `greenie` with UID 4000
- Verify user creation using Ansible ad-hoc commands

## Lab 2 – Advanced Automation with Roles

### Jenkins Role
- Installs Jenkins CI/CD server
- Ensures service is running and enabled

### MariaDB Server
- Installs and configures MariaDB
- Uses Ansible Vault for secure root password
- Applies custom configuration safely
- Ensures idempotent deployment

## Security Features
- SSH key-based authentication
- Ansible Vault for sensitive data
- Privilege escalation using become

## Key Concepts
- Inventory management
- Playbooks and roles
- Idempotency
- Service automation
- Configuration management

## How to Run

Lab 1:
ansible-playbook playbook.yml -i inventory --become

Lab 2:
ansible-playbook site.yml --ask-vault-pass
