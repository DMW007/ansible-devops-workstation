# Ansible Dev(Ops) Workstation

Setup any Ubuntu machine for working with common DevOps tools. Supports Ubuntu 18.04 LTS and higher.

## Features & software

- Terraform with KVM plugin
- KVM
- VirtualBox
- Visual Studio Code
- Supports installation behind corporate proxy
- Local squid proxy as reverse proxy for corporate proxy
- Fetch MITM root certificate from corporate proxy

Some usefull CLI tools:

- Git
- bmon (Network traffic overview)
- jq (JSON parsing)

## Preparation on the target system

- Python and Ansible: Could be installed by executing `./install-requirements.txt`
- User has sudo permission without password: Add `<username> ALL=(ALL) NOPASSWD: ALL` to `visudo`
- SSH access via SSH-Key (copy with e.g. `ssh-copy-id user@localhost` when running locally)

## How to provision

```bash
ansible-playbook -i <target-system> [-u username] ansible-devops-workstation.yml -v
```
