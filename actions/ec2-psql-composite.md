# EC2 with PSQL Client Composite Action

This composite action deploys an EC2 instance and installs the PostgreSQL client on it.

## Inputs

- `aws_region`: AWS region (default: 'ap-southeast-2')
- `ami_id`: AMI ID for the EC2 instance
- `instance_type`: Instance type for the EC2 instance (default: 't2.micro')
- `key_name`: Name of the SSH key pair
- `instance_name`: Name tag for the EC2 instance (default: 'Demo Instance')
- `ssh_user`: SSH username
- `ssh_private_key`: SSH private key

## Outputs

- `instance_id`: ID of the created EC2 instance
- `instance_public_ip`: Public IP of the created EC2 instance

## Example usage

```yaml
- name: Deploy EC2 with PSQL Client
  uses: demodso/org-action-ec2-psql-composite@v1
  with:
    aws_region: "ap-southeast-2"
    ami_id: "ami-0c55b159cbfafe1f0"
    instance_type: "t2.micro"
    key_name: "your-key-pair-name"
    instance_name: "My EC2 Instance"
    ssh_user: "ec2-user"
    ssh_private_key: ${{ secrets.SSH_PRIVATE_KEY }}
```
