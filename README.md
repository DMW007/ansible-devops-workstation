## Preparation on the target system
- Python for Ansible
- User has sudo permission without password: Add `<username> ALL=(ALL) NOPASSWD: ALL` to `visudo`

## How to provision

```bash
ansible-playbook -i <target-system> [-u username] ansible-dev-vm.yml -v
```