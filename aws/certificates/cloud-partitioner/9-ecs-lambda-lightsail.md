# 9

## ecs

- docker: container that run on any OS
- ecr (elastic container registry)
- many container on one server
- ECS = elastic container service, aws lauch and stop containers

## fargate
- launch docker container on aws, and do not provision ant infra no ec2
- serverless offering, aws run container based on cpu / ram used

## serverless
- dev dont have to manage server anymore
- just deploy code, function
- s3, dynamodb, fargate, lambda are serverless

## lambda
- serverless, function as a service
- run on demand, event driven (triggered)
- pay per calls/durations
- has time limit

## api gateway
- build a serverless api
- restful and websocket api

## aws batch
- batch processing computing
- launch ec2 instance or spot instance, ebs . instance store
- batch job defined as docker images and run on ECS
- no need to provision resources

## lightsail
- all in one for non tech

