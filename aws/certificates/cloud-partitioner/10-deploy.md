# Deployment

## CloudFormation

- IaC
- use yaml file

## Cloud Development Kit (CDK)

## Beanstalk
- platform as a service
- just application code is responbility of developer
- single instance
- LB + ASG
- ASG only
- has cloudwatch monitor

## CodeDeploy
- works on ec2 and onprem

## CodeBuild
- serveless build and test

## CodePipeline
- build test deploy to beanstalk


## CodeArtifact
- software packages
- maven, gradle, npm yarn can talk to this

## System Manager (SSM)
- managed instance and patch server
- hybrid, works with on prem

## ssm session manager
- no ssh access, bastion need
- start a secure shell on ec2

## ssm parameter store
- api key, ssh key