# Global application

## Regions or Edge location
- decrease latency
- disaster recovery

## regions
- for deploy app and infra

## az
- made of multiple data center

## edge location (point of presense)
- for content delivery as close as possible to users

## route53
- a managed DNS (domain name system), phone book, reach server via url
- url to ip4/6 to a record 
- simple routing policy (no health checks)
- weighted routing policy
    - distributed weight of traffic to ec2 
- latency routing policy
- failover routing policy
    - disaster recovery
    - health check 

## CloudFront
- content delivery network CDN
- cached at Edge location
- DDoS protection
- 216 edge location

- originas
    - S3, Origin Access Control 
    - custom Origin HTTP

## S3 Transfer Acceleration

## AWS Global Accelerator
- improve performance and reliability of application
- use aws internal network to route your application
- vs CloudFront, no caching, proxying packet, good for http

## AWS Outpost
- hybrid Cloud
- server racks
- set up and manage outpost racks within your on-premises infra

## aws wavelength
- 5G network

## aws local zone
- closer to end users to run latency sensitive applicatio, extend your vpc to more location

## cloud intergration

## sqs
- simple queue service, message queue
- decouple application, serverless
- FIFO queue, or standard queue (at least once delivery), no order is preserved

## sns
- pub sub models, notification service
- topic, event publisher and subscriber

## kinesis
- real-time big data streaming
- collect and process streaminh

## aws mq
- managed broker service for rabbitMQ and activeMQ
- cannot scale
- has both queue features and topic features

