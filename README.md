# AWS IAM Role and Policy Setup for Least-Privilege Access

This project demonstrates how to create an AWS IAM role and policy to follow the principle of least privilege. The policy allows an EC2 instance to read objects from a specific S3 bucket without granting unnecessary permissions. This setup provides a secure and controlled way to manage access to S3 resources.

## Project Overview

### Objective
The goal of this project is to:
- Create a restricted IAM policy to allow read-only access to a specific S3 bucket.
- Attach the policy to an IAM role.
- Apply the role to an EC2 instance to control its access.

### Why Least Privilege?
The principle of least privilege means granting only the permissions needed to perform a specific task. This helps:
- Reduce the risk of unauthorized access.
- Limit potential damage in case of a security incident.
- Simplify access management by restricting permissions to essential actions.


#### Policy JSON Example
The policy JSON file is available [here](policy.json).
