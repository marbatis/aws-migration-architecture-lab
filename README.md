# AWS Migration Architecture Lab

Private working repository for an AWS migration architecture exercise.

## Contents

- `diagrams/aws-migration-architecture.drawio` - editable diagrams.net source file.
- `diagrams/aws-migration-architecture.png` - high-resolution rendered diagram.
- `diagrams/aws-migration-architecture.pdf` - PDF export.

## Architecture Summary

The diagram models a migration architecture with:

- CloudFront serving a static frontend hosted in Amazon S3.
- Internet traffic entering a VPC through an Internet Gateway.
- An internet-facing Application Load Balancer in public subnets across two Availability Zones.
- An Auto Scaling Group running EC2 application instances in private application subnets.
- Amazon RDS MySQL Multi-AZ in private database subnets.
- An analytics flow from on-premises data through AWS DataSync into an Amazon S3 data lake.
- Amazon EMR processing inside the VPC and writing results back to S3 for Amazon QuickSight.

## Security Note

This repository intentionally contains architecture artifacts only. It does not include AWS credentials, access keys, secret keys, private keys, Terraform state, local environment files, or database passwords.

