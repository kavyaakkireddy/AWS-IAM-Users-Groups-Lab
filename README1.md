# AWS IAM Users and Groups Lab

## Objective
To create IAM users and groups, assign permissions using IAM policies, and verify access to AWS S3 and EC2 services.

## Tools Used
- Amazon Web Services (AWS)
- AWS IAM
- Amazon S3
- Amazon EC2
- GitHub

## Tasks Performed

### Task 1: Inspect IAM Users and Groups
- Checked the existing IAM users and their permissions.
- Verified that user-1 had no directly assigned permissions and was not part of a group.
- Inspected the policies attached to the EC2-Support, S3-Support, and EC2-Admin groups.

### Task 2: Add Users to Groups

| IAM User | Group | Permissions 
| user-1 | S3-Support | AmazonS3ReadOnlyAccess |
| user-2 | EC2-Support | AmazonEC2ReadOnlyAccess |
| user-3 | EC2-Admin | Describe, start, and stop EC2 instances |

### Task 3: Verify Permissions

**user-1 — S3 Support**
- Can list and view S3 buckets, subject to resource policies.
- Cannot access EC2 operations without appropriate permissions.

**user-2 — EC2 Support**
- Can view EC2 resources.
- Cannot start or stop EC2 instances.
- Cannot access S3 without appropriate permissions.

**user-3 — EC2 Admin**
- Can describe, start, and stop EC2 instances, subject to the configured policy and resource conditions.

## Result
The IAM users were assigned to their respective groups, and the permissions were tested to demonstrate role-based access control through group membership.

## Evidence
Screenshots of group membership, attached policies, and permission verification will be added after completing the lab.
