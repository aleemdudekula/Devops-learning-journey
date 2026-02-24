# Write a script to report the usage of AWS project

## Description: 

---> submit report to Manager 

---> for that we can do manually its difficult every time go and login aws console

---> Every Day submitted the report 

---> solution do autamation using scripting 

---> using cronjob we ran script on every day in certain time (6pm)

---> before that you can install & configure aws cli in your are terminal 
     cmd : sudo apt install aws cli
           aws configure (aws access key id & aws secret access key)

## script prepare:

---> create a file aws-resource-tracker.sh

script:
```
#!/bin/bash
###############################################
# Author: Aleem dudekula
# Date : 24th-Feb 2026
# version: 
# This script will report the aws resource usage
################################################
# AWS S3
# AWS EC2
# AWS IAM users
# AWS Lambda 
set -X
# list S3 buckets
echo "print list of S3 buckets"
aws s3 ls
# list EC2 Instances
echo "print list of ec2 instances"
aws ec2 describe-instances | jq '.Reservations[].Instances[].InstanceId'
# list lambda 
echo "print list of lambda functions"
aws lambda list-functions
#list IAM users
echo "print list of IAM users"
aws iam list-users

./aws-resource-tracker.sh | more
before that check file permissions #ls -lst










