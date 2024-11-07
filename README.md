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

![Screenshot of IAM Console](image )

## Steps to Reproduce

### 2. Create an IAM Role
Follow these steps to create an IAM role for EC2 with a least-privilege policy attached.

1. **Navigate to the IAM Console**  
   - Go to the IAM Console in AWS.
   - In the left sidebar, click on **Roles**.

2. **Create a New Role**  
   - Click on the **Create role** button.

3. **Choose a Trusted Entity (EC2)**  
   - Under **Select trusted entity**, select **AWS service**.
   - In the list of services, select **EC2**, as this role will be used by an EC2 instance.
   - Click **Next**.

4. **Attach the Policy to the Role**  
   - Search for the policy you created (e.g., `ReadOnlyAccessToMyS3Bucket`).
   - Select the policy by checking the box next to it, then click **Next**.

5. **Name and Describe the Role**  
   - Enter a name for the role, such as `EC2ReadOnlyS3Access`, and add a description for future reference.
   - Click **Create Role** to finalize the setup.

6. **Assign the Role to an EC2 Instance (Optional)**  
   - In the **EC2 Console**, select an instance, click on **Actions** > **Security** > **Modify IAM Role**.
   - Choose the role you just created (`EC2ReadOnlyS3Access`) from the dropdown and click **Update IAM role**.

---

This will create an IAM role that grants only the necessary permissions for EC2 instances to access specific S3 resources.



