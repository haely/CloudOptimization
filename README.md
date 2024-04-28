# Cloud Optimization

This document provides an overview of AWS and GCP services, focusing on how costs add up.

## AWS (Amazon Web Services)

- [EC2 (Elastic Compute Cloud)](#aws-ec2)
- [S3 (Simple Storage Service)](#aws-s3)

## GCP (Google Cloud Platform)

- [VM (Virtual Machine compute instancea)](#gcp-vm)
- [GCS (Google Cloud Storage)](#gcs-storage)


---

## AWS EC2

### EC2 Overview/Intended Use

### Intended Use
### Cost breakdown
### Best Practices

## AWS S3

### Intended Use
### Cost breakdown
### Best Practices


---

## GCP VM

### Intended Use
### Cost breakdown
### Best Practices


## GCS Storage
Google Cloud storage
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
