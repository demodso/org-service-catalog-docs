# Infrastructure Wrapper Action

This wrapper action deploys an RDS instance, an EC2 instance, and installs the PostgreSQL client on the EC2 instance.

## Inputs

- `aws_region`: AWS region (default: 'ap-southeast-2')
- `rds_instance_class`: RDS instance class (default: 'db.t3.micro')
- `db_name`: Database name
- `db_username`: Database username
- `db_password`: Database password
- `db_instance_name`: Name tag for the RDS instance (default: 'Demo RDS Instance')
- `ec2_ami_id`: AMI ID for the EC2 instance
- `ec2_instance_type`: Instance type for the EC2 instance (default: 't2.micro')
- `ec2_key_name`: Name of the SSH key pair
- `ec2_instance_name`: Name tag for the EC2 instance (default: 'Demo EC2 Instance')
- `ssh_user`: SSH username
- `ssh_private_key`: SSH private key

## Outputs

- `rds_endpoint`: The connection endpoint for the RDS instance
- `rds_port`: The port the RDS instance is listening on
- `ec2_instance_id`: ID of the created EC2 instance
- `ec2_instance_public_ip`: Public IP of the created EC2 instance

## Example usage

```yaml
- name: Deploy Infrastructure
  uses: demodso/org-action-infra-wrapper@v1
  with:
    aws_region: "ap-southeast-2"
    rds_instance_class: "db.t3.micro"
    db_name: "mydb"
    db_username: ${{ secrets.DB_USERNAME }}
    db_password: ${{ secrets.DB_PASSWORD }}
    db_instance_name: "My RDS Instance"
    ec2_ami_id: "ami-0c55b159cbfafe1f0"
    ec2_instance_type: "t2.micro"
    ec2_key_name: "your-key-pair-name"
    ec2_instance_name: "My EC2 Instance"
    ssh_user: "ec2-user"
    ssh_private_key: ${{ secrets.SSH_PRIVATE_KEY }}
```
