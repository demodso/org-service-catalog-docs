# Ansible PSQL Installation Action

This action installs the PostgreSQL client on a target EC2 instance using Ansible.

## Inputs

- `target_host`: Target host IP or hostname
- `ssh_user`: SSH username
- `ssh_private_key`: SSH private key

## Example usage

```yaml
- name: Install PSQL Client
  uses: demodso/org-action-ansible-psql@v1
  with:
    target_host: ${{ steps.ec2-deploy.outputs.instance_public_ip }}
    ssh_user: "ec2-user"
    ssh_private_key: ${{ secrets.SSH_PRIVATE_KEY }}
```
