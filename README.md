# Ansible Dev(Ops) VM

Setup any Ubuntu machine for common DevOps tools.

## Features & software

- Terraform with KVM plugin
- KVM
- VirtualBox
- Supports installation behind corporate proxy
- Local squid proxy as reverse proxy for corporate proxy
- Fetch MITM root certificate from corporate proxy

## Preparation on the target system

- Python for Ansible
- User has sudo permission without password: Add `<username> ALL=(ALL) NOPASSWD: ALL` to `visudo`

## How to provision

```bash
ansible-playbook -i <target-system> [-u username] ansible-dev-vm.yml -v
```
