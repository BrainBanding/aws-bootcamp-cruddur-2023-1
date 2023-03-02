# Week 0 — Billing and Architecture

## Required Homework

### Install AWS CLI

1. Copy Template and give it a name **aws-bootcamp-cruddur-2023**
2. Install the AWS CLI reference :[**AWS CLI Install Instructions**] https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
3. I did uprated the `.gitpod.yml` to include the following task.

```sh
tasks:
  - name: aws-cli
    env:
      AWS_CLI_AUTO_PROMPT: on-partial
    init: |
      cd /workspace
      curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
      unzip awscliv2.zip
      sudo ./aws/install
      cd $THEIA_WORKSPACE_ROOT
```
###Created New user and Generated credentials

1. Go to(IAM Users Console](https://us-east-1.console.aws.amazon.com/iamv2/home?region=us-east-1#/users) aws-lon create a new user
2. `Enable console access` for the user
3. Create a new `Admin` Group and apply `AdministratorAccess`
4. Create the user and go find and click into the user
5. Click on `Security Credentials` and `Create Access Key`
6. Choose AWS CLI Access
7. Download the CSV with the credentials

##Set ENV
I set credentials for the current bash terminal
```
export AWS_ACCESS_KEY_ID=""
export AWS_SECRET_ACCESS_KEY=""
export AWS_DEFAULT_REGION=eu-west-2
```
- ![Credentials](assets/AWS-Gitpod.png)

Gitpod to remember these credentials if we relaunch our workspaces
```
gp env AWS_ACCESS_KEY_ID=""
gp env AWS_SECRET_ACCESS_KEY=""
gp env AWS_DEFAULT_REGION=eu-west-2
```
- ![
