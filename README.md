
# My Personal Portfolio Infrastructure

## Using this infrastructure

### Install AWS CDK

1. [Create a AWS account.](https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-creating.html)

2. [Install the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

3. [Configure your AWS account.](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-quickstart.html)
   ```bash
   aws configure
   ```

4. [Install AWS Cloud Development Kit (CDK) v2](https://docs.aws.amazon.com/cdk/v2/guide/getting_started.html)

5. [Bootstrap your environment:](https://docs.aws.amazon.com/cdk/v2/guide/bootstrapping.html)
    ```bash
    cdk bootstrap
    ```

### DNS Setup 

Skip this section if you do not wish to use your own domain name.

If you would like to purchase your own domain name through AWS Route53 follow this official [AWS Guide](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/domain-register.html#domain-register-procedure).

1. If you do not already have a hosted zone in Route53 ([AWS Guide](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/CreatingHostedZone.html))
   1. Go to [Route53](console.aws.amazon.com/route53)
   2. If you're new to Route 53, choose Get started under DNS management. 
   3. If you're already using Route 53, choose `Hosted zones` in the navigation pane. 
   4. Choose `Create hosted zone`. 
   5. In the Create Hosted Zone pane, enter the name of the domain that you want to route traffic for. You can also optionally enter a comment. 
   7. For Type, accept the default value of Public Hosted Zone. 
   8. Choose `Create`.

2. Update domain name servers ([AWS Guide](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/domain-name-servers-glue-records.html#domain-name-servers-glue-records-adding-changing))
   1. Go to [Route53](console.aws.amazon.com/route53)
   2. In the navigation pane, choose `Registered Domains`. 
   3. Choose the name of the domain for which you want to edit settings.
   4. Choose `Add or edit name servers`.
   5. Replace the name servers with the name servers for the Route 53 hosted zone.

### Deployment

Decide which architecture you would like to deploy and follow the instructions found in the respective repository.
