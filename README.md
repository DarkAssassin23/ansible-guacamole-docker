# Guacamole Docker Compose with Ansible

## About
An Ansible playbook to deploy Guacamole with Docker Compose

## Setup
1. Install Ansible
2. Rename `example.config.yml` and `example.inventory.ini` to `config.yml`
   and `inventory.ini` respectively, and modify them as desired. 

## Usage
```bash
ansible-playbook main.yml -i inventory.ini -K
```
