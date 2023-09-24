# Terraform Beginner Bootcamp 2023

## Semantic Versioning :mage:

This project is going to utilize semantic versioning for its tagging. 

[semver.org](https://semver.org/)

The general format:

**MAJOR.MINOR.PATCH**, eg. `1.0.1`

- **MAJOR** version when you make incompatible API changes
- **MINOR** version when you add functionality in a backward compatible manner
- **PATCH** version when you make backward compatible bug fixes

## Installing the Terraform CLI

The Terraform CLI installation instructions have changed due to gpg keyring changes. so we needed to refer to the latest install instructions from Terraform documentation to change the scripting for install.
[Install Terraform CLI](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)

### Refactoring 

[](https://www.cyberciti.biz/faq/)
https://www.cyberciti.biz/faq/how-to-check-os-version-in-linux-command-line/
https://en.wikipedia.org/wiki/Shebang_(Unix)
https://en.wikipedia.org/wiki/Chmod
https://www.gitpod.io/docs/configure/workspaces



### Installing AWS CLI

AWS CLI is installed for the project via the bash script [`./bin/install_aws_cli`](./bin/install_aws_cli)

[Getting started install AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)


[AWS CLI env vars](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-envvars.html)


We can check if our AWS credentials are configured correctly by running the following command:

```sh
aws sts get-caller-identity
```

If it's successful you should see a json payload return that looks like this:

```json
{
    "UserId": "",
    "Account": "",
    "Arn": ""
}

We'll need to generate AWS CLI credits from IAM user in order to use AWS CLI