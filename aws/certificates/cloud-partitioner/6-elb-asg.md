# 6 Elastic Load Balancing & Auto Scaling Groups

## HA
- vertical: scale the instance size
- horizontal: scale the number of instance
- scalabilityL accomodate larger load by scale up and out
- elasticity: some auto-scaling based on load after system is scalable
- agility: IT resource closer to developer

## Load balancing
- forward traffic to multiple server (ec2)
- single point of access (DNS)
- do regular health check to instance
- provide HA

## ELB (Elastic load balancer)
- managed load balancer
- aws: upgrades, maintaince, HA
- type
    - ALB (HTTP/HTTPS/gRPC only)- layer 7
        - static DNS (url)
        - http routing features
        - route to target group ( of ec2)
    - NLB (allows for TCP/UDP) - layer 4
        - high perf, low latency
        - static Elastic IP
    - gateway load balancer - layer 3
        - GENEVE proctocol on IP packets
        - route traffic to firewalls for intrusion detection

## ASG
- auto scaling group
- min, max, auto-register ec2 and replace unhealthy, desire amount
- timeout, unhealthy threhold, health check protoco.

- scaling strategies
    - step scaling
        - trigger, then add/remove n
    - target tracking scaling
        - avg cpu stay of n%
    - scheduled scaling
        - for known usage patterns

    - predictive scaling
        - use ML to predict
        - time based pattern
