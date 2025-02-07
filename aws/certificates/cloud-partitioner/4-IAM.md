# 4. IAM

## 1. Intro

- Users
- Groups
- Policies

## 2. Users

- Long term password
- Root users created automatically

## 3. Policies

- Versions (policy language version), Id, Statement
- Statements consist of
  - sid (optional): identifier for the statement, int
  - effect: Allow, Deny
  - principal: account/user/role to which this policy applied to
  - action: list of actions 
  - resources: list of resources to which the actions applied to
  - conditions (optional)

- MFA

- Access keys, cli, and SDK: 3 option to access AWS


- Access key ID: username, secret access key: password

- IAM role: for EC2 instance, lambda, or others

- IAM Security tool
  - Iam credential report: account level
  - Iam Last Access: user-level

- one physical user = one aws user

- dont use root account except set up 

