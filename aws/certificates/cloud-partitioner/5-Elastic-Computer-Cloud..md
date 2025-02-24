# 5-EC2

## Basics
- config: OS, CPU, RAM, EBS/EFS or Instance Store, network card
- firewall rules (security group) 
    - allow ssh traffic
    - allow http(s) traffic from internet

- boostrap script (ec2 user data)
    - as a root user
    - run once at start up time

- t2.micro is free

- public IPv4 and private

- stop vs terminate the instance

## Instnace Type
- instance class + generation . size within the instance class
    - m5.2xlarge

- Types
    - general purpose
    - compute optimized (c)
    - memory optimized (R for ram)
        - in memory db
    - storage optimized (i or d)
        - caching using redis in memory

## Security Groups
Controls traffic into or out of EC2

- ONLY contains allow rules
- groups rules can be reference by IP or by security group
- can be attach to many instance
- locked down to a region/VPC combination
- by defauly, inbound is blocked, outbound is authorised 

### portal
- 22: ssh (shell)
- 21: ftp (file transfer)
- 22: Sftp (secure)
- 90: http
- 443: https (secure)
- 3389: RDP (remote desktop)

## How to SSH

```
chmod 0400 your.pem
ssh ec2-user@publicIP -i your.pem
logout
```

or using EC2 Connect session in browser

## Pricing

- on-demand, pay be second
- reserved, 1 to 3 year
- saving plan
- spot instance, can lose instance
- dedicated host, a physical server and compliance
- dedicated intsance, run on hardware by your self

## shared res
- aws
    - infra
    - isolation on host
    - hardware

- user
    - security 
    - os


## EC2 Storage

### EBS Volume

- Elastic Block Store
    - network drive that attach, alloow instance to persist data after termination
    - mount to one instance at a time and bound to specific AZ
    - not a physical driver, use network
    - lock in a AZ, has a size in GP and IOPS fixed
    - delete on termination by default (root)

- General Purpose (GP)

- EBS snapshot
    - make a backup of ebs at a point 
    - can copy over AZ or region
    - snapshot archive (takes 72 horus to restore)
    - recycle bin (1 day to 1 yr)

### AMI 
Amazon Machine Image

- customiztion of an EC2: OS, minitoring, config, software
- pre-packaged, faster boot
- region specific

- Public AMI vs own AMI
- build an AMI will create snapshot
- crreating images from ec2, tag it, and use it for other 

### Image Build
- used to automate the creation of VM or container images
- create, validate and test ec2 AMI

### Instance Store
- hardware disk, better IO, lose storage if instance stop
- good for buffer, cache, scratch

### EFS: elastic file system
- managed NFS (network file system), mounted on 100 of EC2
- only with Linux in multi-AZ
- expansive 3x gp2, pay per use
- a shared file system
- EFS-IA (infrequent access)

### shared res
- aws: infra, replica for data for ebs, efs
- consumer: backup, data encryption, data stored

### FSx (3rd party fs)