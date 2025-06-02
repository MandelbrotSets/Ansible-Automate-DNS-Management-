# DNS Automation with Ansible

Automates DNS record management on Linux DNS servers using Ansible playbooks.

## Features
- Add/remove DNS A records via `nsupdate`
- Idempotent playbooks for safe re-execution
- Ready for integration with AWX/Tower

## Prerequisites
- Ansible 2.9+
- BIND DNS server with `nsupdate` configured
- SSH access to DNS servers

## Usage
1. Edit `inventories/dns_servers.yml` with your server IPs
2. Modify records in `playbooks/manage_dns.yml`
3. Run:
   ```bash
   ansible-playbook -i inventories/dns_servers.yml playbooks/manage_dns.yml

## Project Structure
   .
├── inventories/
│   └── dns_servers.yml    # Server inventory
└── playbooks/
    └── manage_dns.yml     # Main playbook
