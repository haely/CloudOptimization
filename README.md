# Cloud Optimization

This document provides an overview of AWS and GCP services, focusing on how costs add up.

## AWS (Amazon Web Services)

- [Compute Instances, EC2](#compute-instances-or-aws-ec2)
- [GCS, S3](#google-cloud-storage-or-aws-s3)
- [Cloud functions, Lambda](#cloud-functions-or-aws-lambda)



---

## Compute Instances or AWS EC2

### Intended Use
Virtual servers, but you pay for what is rented even when you do not use the rental. <br>
Elastic IPs, NAT gateway, persistent storage costs add up pretty fast. <br>
Termnating an instance, deleting one still won't free up the IPs. <br>

Clean up = a full clean up. Under the table, behind the curtains, in the garage etc. Hah! reminds me of the fun times when on lease end, a bunch of us did not clean up the garage. Those trask pick-up costs pile up!!

### Cost breakdown
1. Everything
### Best Practices
1. Choose the right instance type for your needs (don't overpay for more power than you need).
2. Use Auto Scaling to automatically adjust capacity based on demand.
3. Terminate unused instances to avoid unnecessary costs.
4. Check periodically if firecasted usage needs to be updated.

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
A quick (and this is key) 'quick' function to do some stuff on your resources. AWS Lambda has a default timeout of 15 minutes. If a function is not tested thoroughly and has runtime erros, you will be charged for all those 15 mins, get no result, and if you are calling this function every hour, phew.. rinse, repeat!


### Cost breakdown
1. Invocation frequency
2. Run time


### Best Practices
A resource clean up should always involve cross-resource check. The bucket you are deleting or the instance you are terminating can have a lambda function attached. If left as it was, the lambda function costs spike up fast.

