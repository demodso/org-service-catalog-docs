# RDS Deployment Action

This action deploys a PostgreSQL RDS instance using Terraform.

## Inputs

- `aws_region`: AWS region (default: 'ap-southeast-2')
- `instance_class`: RDS instance class (default: 'db.t3.micro')
- `db_name`: Database name
- `db_username`: Database username
- `db_password`: Database password
- `db_instance_name`: Name tag for the RDS instance (default: 'Demo RDS Instance')

## Outputs

- `rds_endpoint`: The connection endpoint for the RDS instance
- `rds_port`: The port the RDS instance is listening on

## Example usage

```yaml
- name: Deploy RDS Instance
  uses: demodso/org-action-rds-deploy@v1
  with:
    aws_region: "ap-southeast-2"
    instance_class: "db.t3.micro"
    db_name: "mydb"
    db_username: ${{ secrets.DB_USERNAME }}
    db_password: ${{ secrets.DB_PASSWORD }}
    db_instance_name: "My RDS Instance"
```
