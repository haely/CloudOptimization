# Cloud Optimization

This document provides an overview of AWS and GCP services, focusing on how costs add up.

## AWS (Amazon Web Services)

- [Compute Instances, EC2](#compute-instances-or-aws-ec2)
- [GCS, S3](#google-cloud-storage-or-aws-s3)
- [Cloud functions, Lambda](#cloud-functions-or-aws-lambda)



---

## Compute Instances or AWS EC2

### Intended Use
### Cost breakdown
### Best Practices

## Google Cloud Storage or AWS S3

Google Cloud storage, AWS S3 Buckets
### Intended Use
Object/Log storage, DXata archive/backup
### Cost breakdown
1. Data Storage (size, region, tiers etc0
2. Data Processing - retrieving to a warmer tier
3. Network cost - reading, writing data from/to buckets

### Best Practices
1. Data Archiving - Move less frequently used data to colder tiers (Lifecycle policies)
2. Data Deletion - Delete data which won't be used in the future.
3. AutoClass - Moves objects to the appropriate tiers, additional costs fr management
4. Object compression and caching for frquently used data

### Common commands


## Cloud Functions or AWS Lambda

### Intended Use
### Cost breakdown
### Best Practices
