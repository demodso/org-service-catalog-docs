# Infra Demo Service List

Welcome to the Infra Demo Service List. This documentation provides information on how to use our custom GitHub Actions for infrastructure deployment.

## Available Actions

- [EC2 Deployment](actions/ec2-deploy.md)
- [RDS Deployment](actions/rds-deploy.md)
- [Ansible PSQL Installation](actions/ansible-psql.md)
- [EC2 with PSQL Client](actions/ec2-psql-composite.md)
- [Infrastructure Wrapper](actions/infra-wrapper.md)

## Getting Started

To use these actions in your workflows, refer to the individual action documentation for specific usage instructions and examples. All actions are designed to work with AWS and use OIDC for secure authentication.

## Prerequisites

1. AWS account with appropriate permissions
2. GitHub repository within the Infra Demo organization
3. OIDC connection set up between GitHub and AWS

For more information on setting up OIDC, see [Configuring OpenID Connect in Amazon Web Services](https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/configuring-openid-connect-in-amazon-web-services).

## Support

If you encounter any issues or have questions, please open an issue in the respective action's repository.
