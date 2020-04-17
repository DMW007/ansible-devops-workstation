# Ansible Dev(Ops) Workstation

Setup any Ubuntu machine for working with common DevOps tools.

## Features & software

- Terraform with KVM plugin
- KVM
- VirtualBox
- Supports installation behind corporate proxy
- Local squid proxy as reverse proxy for corporate proxy
- Fetch MITM root certificate from corporate proxy

Some usefull CLI tools:

- Git
- bmon (Network traffic overview)
- jq (JSON parsing)

## Preparation on the target system

- Python for Ansible
- User has sudo permission without password: Add `<username> ALL=(ALL) NOPASSWD: ALL` to `visudo`

## How to provision

```bash
ansible-playbook -i <target-system> [-u username] ansible-devops-workstation.yml -v
```
