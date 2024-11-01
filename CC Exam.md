# IAM - Cryptography
## Cybersecurity Basics
- **Definition**: Protection of digital information from unauthorized access, harm, or misuse.
- **CIA Triad**:
  - **Confidentiality**: Keeps information private; only authorized users have access.
  - **Integrity**: Maintains accuracy and reliability of information.
  - **Availability**: Ensures information is accessible for authorized users.
### Extended CIA Concepts
- **Authentication**: Verifies user/system identity to access a resource.
- **Authorization**: Determines permitted actions or resources for authenticated users.
- **Non-Repudiation**: Ensures users cannot deny involvement in digital transactions.
## Cryptography
- **Definition**: Practice of secure communication in the presence of adversaries.
- **Goal**: Ensure information is accessible only to intended recipients.

![Pasted image 20241027163927.png](Cloud%20Computing%20%20Exam%20Notes-media/7123e0d37035c3fce7709a96dd85fe8f5ff21817.png "wikilink")

### Types of Ciphers
- **Caesar Cipher**: Substitution cipher where each letter is shifted by a set number of positions.
  - **Example**: `HELLO` (shift by 3) becomes `KHOOR`.
  - **ROT3**: A shift of 3 positions in the alphabet.
	- **Security flaw**: to brute force attack by enumeration (all possible rotations) – 25 meaningful shifts (26 letters)
  
![Pasted image 20241027164103.png](Cloud%20Computing%20%20Exam%20Notes-media/a7da9c86105635d6db8aa70432a293c4fcdeacb4.png "wikilink")

## Cryptography Today
### Symmetric Key Cryptography
- **Definition**: The same key is used for both encryption and decryption.
- **Process**:
  - **Encryption**: Converts plaintext to ciphertext.
  - **Decryption**: Reverses ciphertext to plaintext.
- **Examples**:
  - **DES** (insecure), **3DES** (insecure), **AES** (AES-128, AES-192, AES-256 - larger key space, impossible to enumerate key space).
- **Applications**: Data encryption (files, network packets).
![Pasted image 20241027164125.png](Cloud%20Computing%20%20Exam%20Notes-media/23c0d71f4e7ce95886871b676c3a04086895280c.png "wikilink")

### Asymmetric Key Cryptography
- **Definition**: Uses a pair of distinct keys (public and private) for encryption and decryption.
- **Process**:
  - **Public Key**: Used for encryption.
  - **Private Key**: Used for decryption.
- **Examples**:
  - **ECC**, **RSA**
- **Applications**: Remote authentication (e.g., SSH).
![Pasted image 20241027164447.png](Cloud%20Computing%20%20Exam%20Notes-media/654149996527b77ba91001eaf07d259240f1d744.png "wikilink")

## Hash Functions
- **Definition**: Takes an input and transforms it into a fixed-size hash digest.
- **Properties**:
  - Same input produces the same hash.
  - Small input changes lead to significant hash changes.
- **Examples**:
  - **MD5** (insecure), **SHA-1** (insecure), **SHA-256** (secure).

![Pasted image 20241027164538.png](Cloud%20Computing%20%20Exam%20Notes-media/6d02d73ac5392ece0c45ffc7af46eb8bf6758073.png "wikilink")

#### SHA 256
**Purpose:** Used to verify integrity of information provided.

![Pasted image 20241027165055.png](Cloud%20Computing%20%20Exam%20Notes-media/3378574a11f1dab4f47bb91321999cc114de6c32.png "wikilink")

### Hash Collisions
- **Definition**: Two different inputs producing the same hash (hash digest).
- **Cause**: Finite output possibilities but infinite input possibilities (Pigeonhole Principle).
- **Examples**: Common with MD5 and SHA-1.

![Pasted image 20241027165405.png](Cloud%20Computing%20%20Exam%20Notes-media/367164dff2b41f839cb20989d55ec1af613ea3ce.png "wikilink")

### Pigeonhole Principle
- **Analogy**: 10 pigeons but only 9 holes. If n items are put into m containers, with n > m, then at least one container must contain more than one item.
- **Concept**: If more items (inputs) than containers (possible hash combinations) exist, at least one container holds multiple items.
- **Implication**: Hash collisions are inevitable due to finite hash outputs.
Here's the continuation of the notes for the topic "IAM - Cryptography" in Markdown format, based on the latest screenshot.
## Cryptography Techniques and CIA Triad Protection
- **Cryptography Techniques**:
  - **Symmetric Key Cryptography**
  - **Asymmetric Key Cryptography**
  - **Hash Functions**
- **CIA Triad Protection by Cryptography**:
  - **Confidentiality**: Ensured by **Symmetric Key** and **Asymmetric Key** cryptography.
  - **Integrity**: Maintained using **Hash Functions** (e.g., SHA-2, SHA-256).
  - **Availability**: Not protected by cryptography; attackers can disrupt availability by intercepting or blocking data (plaintext or ciphertext).
*Note: Cryptography focuses on confidentiality and integrity but does not ensure data availability.*
# IAM - Identity Access Management
## What is IAM?
- **Definition**: A web service that controls access to AWS resources securely.
- **Purpose**: Manages authentication (who signs in) and authorization (permissions) for AWS resources.
- **Root User**: Has complete access to all AWS resources in an account.

![Pasted image 20241027171312.png](Cloud%20Computing%20%20Exam%20Notes-media/2ad76e2480f6d00df1141e89875351e171c5d0b3.png "wikilink")

## IAM Identity Types
- **IAM User**: Represents a single person/application with specific permissions.
  - **Example ARN**: `arn:aws:iam::accountNumber:user/<userName>`
		e.g., arn:aws:iam::489389878001:user/12345678@student.uwa.edu.au

- **IAM User Group**: Group of users with identical permissions.
  - **Example ARN**: `arn:aws:iam::accountNumber:group/<groupName>`
		e.g., arn:aws:iam::489389878001:group/admins
  - **Note**: Users can belong to multiple groups.
- **IAM Role**: Temporary identity granting specific permissions for tasks, not tied to a single user.
  - **Example ARN**: `arn:aws:iam::accountNumber:role/<roleName>`
		e.g., arn:aws:iam:: 489389878001 :role/apps4ec2
  - **Use Case**: Granting an EC2 instance permissions to access S3.
*Implication of Misuse*: Assigning excessive permissions can lead to unauthorized access, compromising account security.
## How IAM Works
**Principal**: a person or application that uses an IAM user, a root user, or an IAM role to sign in and make requests to AWS.
1. **Authenticate**: Verifies the identity of the principal (user/role).
3. **Authorize**: Determines permissions for the authenticated principal.
4. **Take Action**: Allows or denies actions on AWS resources.
*Example*: Federated users authenticate through external providers (e.g., Google, Facebook, SSO).
**1**: Different principals need to be authenticated by AWS before they can perform actions. Federated user: authenticated by external applications e.g. Gmail, Facebook, Single Sign On
**2**: Authorization is implemented by policies, policies define permissions
**3**: Principals can perform operations such as Stop, delete, create etc.

![Pasted image 20241027171751.png](Cloud%20Computing%20%20Exam%20Notes-media/eadbb56e43636ea111f872dc02db7085fefe00a5.png "wikilink")

## Main Features of IAM
- **Shared Access to Root User**: Grants access to resources in root user account without sharing passwords or keys, reducing security risks.
- **Granular Permissions**: Assigns varying levels of access to different individuals for specific resources. If ARN is deleted, so is the permissions
  - **Example**: Full access to EC2 for one user, read-only access to S3 for another.
## Policies and Permissions
- **Definition**: Policies control access (authorization) by attaching permissions to IAM identities (users, user groups, roles) or AWS resources.
- **Policy Scope**:
  - Defines actions allowed across all access methods (AWS Console, CLI, SDK).
- **Policy Types**:
  - **Identity-Based**: Assigned to IAM users, groups, or roles.
  - **Resource-Based**: Attached to AWS resources.
  - **Permissions Boundary**: Limits maximum permissions.
*Example*: If a policy allows `GetUser`, a user can access user details via any access method (AWS Console, CLI, AWS SDK).
## Identity-Based Policy
- **Controls**: What an identity can do in AWS.
-  **Managed policy**: standalone identity-based policy that can be attached to multiple users, groups, and roles.
	- **Managed Policy Types**:
	  - **AWS Managed Policy**: Created and managed by AWS.
	  - **Customer Managed Policy**: Created and managed by authorized AWS users.
	  - **Inline Policy**: One-to-one relationship between policy and identity. Directly attached to an identity, deleted with the identity.
*Implication of Misuse*: Poorly defined policies can lead to unauthorized access, increasing security risks.
## AWS Managed Policy Types
- **Full-Access Managed Policy**: Grants  permissions for administors by granting full access to all services.
- **Power-User Managed Policy**: Full access to services and resource without user/group management. i.e. subset of full-access managed policy.
- **Partial-User Managed Policy**: Restricted to specific services or actions. i.e. subset of power-user managed policy

![Pasted image 20241027175057.png](Cloud%20Computing%20%20Exam%20Notes-media/fd0564334f60214913c893507fb4c0bdfe8464a2.png "wikilink")

## Administrator Access Policy Structure
- **Version**: Specifies policy language version.
- **Statement**: Defines the permission rule.
- **Effect**: Specifies `Allow` or `Deny` for actions.
- **Action**: Lists allowed or denied operations a user/application can perform.
- **Resource**: Specifies resources affected by the policy. ARN is often used.
*Example JSON*:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "*",
      "Resource": "*"
    }
  ]
}
```
*Note*: No specific principal defined. Attaching this to a principal grants full administrator access.
Here are the notes for the topic "IAM - Identity Access Management Continued" in Markdown format based on the provided screenshots.
## PowerUserAccess Policy
- **Organizations**: Service to consolidate multiple AWS accounts into an organizational structure.
- **Policy Permissions**:
  - Allows all actions on all resources except IAM, Organizations, and Account management.
  - Specifically allows:
    - `iam:ListRoles`
    - `organizations:DescribeOrganization`
    - `account:GetAccountInformation`
- **Statement Requirements**: Must have an effect, action, and resource.
- **Policy Effects**:
  1. Allow all actions except specified restricted ones (IAM, Organizations, Account).
  2. Explicitly allow limited actions for IAM, Organizations, and Account management.
*Example JSON*:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "NotAction": [
        "iam:*",
        "organizations:*",
        "account:*"
      ],
      "Resource": "*"
    },
    {
      "Effect": "Allow",
      "Action": [
        "iam:ListRoles",
        "organizations:DescribeOrganization",
        "account:GetAccountInformation"
      ],
      "Resource": "*"
    }
  ]
}
```
## AWSCloudTrail_ReadOnlyAccess Policy
- **Definition**: Partial User Managed Policy example.
- **CloudTrail**: Service for monitoring user activity and resource usage.
- **Policy Permissions**:
  - Allows actions to get, describe, and list CloudTrail data.
*Example JSON*:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "cloudtrail:Get*",
        "cloudtrail:Describe*",
        "cloudtrail:List*"
      ],
      "Resource": "*"
    }
  ]
}
```
## Customer Managed Policy
- **Definition**: Policies created and managed by AWS account holders.
- **Example Usage**:
  - Group policies like `account-admins-mfa` for Admins.
  - Role-based policies like `EC2-access` for limited resource access.

![Pasted image 20241027183031.png](Cloud%20Computing%20%20Exam%20Notes-media/57712a555f8e6974b6496a4bdc8bb016fd3a029a.png "wikilink")

## Inline Policy
- **Definition**: One-to-one policy directly attached to a single user, group, or role.
- **Usage**: Cannot be shared across multiple entities.
  - **Example**: `DynamoDB-books-app` policy attached to `books-app` role only.
*Note*: Inline policies are deleted if the attached identity is deleted.
**The `DynamoDB-books-app` policy is used by both roles. Is it shared?**
No, because inline policy has one-to-one mapping. cannot have policy on more than one row in the diagram below.

![Pasted image 20241027183732.png](Cloud%20Computing%20%20Exam%20Notes-media/e07beb414c0a62dd9cbec1b93339ffe0696841fd.png "wikilink")

## Resource-Based (Inline) Policy
- **Definition**: Specifies which principal has access to a resource and allowed actions.
- **Example Use Case**: S3 bucket policies controlling who can `GetObject` from a bucket.
- **Note**: All resource policies are inline and deleted if the resource is deleted.
*Example JSON*:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::bucket-name/*"
    }
  ]
}
```
*Implication of Misuse*: Incorrect configuration of resource-based policies could expose resources to unauthorized access.
Here are the notes for the topic "IAM - Identity Access Management Continued" in Markdown format based on the provided screenshots.
## Permissions Boundary
- **Definition**: Sets the maximum permissions an identity-based policy can grant.
- **Example**: A permissions boundary attached to an IAM user named Alice.
- **Effective Permissions**: Intersection between the identity-based policy and permissions boundary defines the actions a user can take.
*Example JSON*:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "s3:*",
        "ec2:*"
      ],
      "Resource": "*"
    }
  ]
}
```
### Permissions Boundary Example
- **Scenario**:
  - Identity-based policy allows `iam:CreateUser`.
  - Permissions boundary only allows `s3:*` and `ec2:*`.
  - **Effective Permission**: Alice cannot create users or manage S3/EC2 resources because there is no intersection between policies.
  
 ![Pasted image 20241028011051.png](Cloud%20Computing%20%20Exam%20Notes-media/1622880a8c473fe5b77ede276507ada06b1cd7f6.png "wikilink")

## IAM - Practice Questions
### **Q1**: Name three keys in a policy and explain their role.
  - **Statement**: Represents a permission rule.
  - **Effect**: Defines if an action is `Allow` or `Deny`.
  - **Action**: Specifies the operations a user/application can perform.
  - **Resource**: Indicates which AWS resources are affected.
  - **Version:** Specifies version of policy syntax and is normally "Version": "2012-10-17"
### **Q2**: Securing Departmental Access to S3 Bucket
#### Scenario: Securing Departmental Access to S3 Bucket
An organization with five departments has organized its IAM users by department using structured paths. Each IAM user is named according to their department, following the pattern `user@department1.company.com`, `user@department2.company.com`, etc. 
The organization’s S3 bucket, `companybucket`, contains separate folders for each department: `department1`, `department2`, `department3`, and so forth. The organization wants to secure the bucket such that:
- **Departmental Write Access**: Users can write only to their own department's folder.
- **Universal Read Access**: All users across the organization can read files from any department folder.
##### Requirements
1. **Granular Access Control**: Only users within a specific department should be able to write to their own folder.
2. **Read Access for All**: Everyone should be able to read from all department folders.
3. **Policy Separation**: To manage permissions effectively, create separate policy statements for each department.
#### Solution: IAM Policy Principles and Example
#### Policy Principles
- **Least Privilege**: Each user is granted only the permissions necessary for their role.
- **Path-Based Access Control**: Use IAM policy paths to limit write permissions based on department folders.
- **Universal Read Access**: Ensure all users can read from any department folder in the bucket.
- **Granularity**: Define specific policy statements for each department, detailing their write access to their own folder.
- **Conditions and Resources in Policy**: Apply `Condition` and `Resource` attributes to target department-specific folders within the bucket.
##### Example IAM Policy (JSON)
JSON policy provides department-specific write access and read access to all users across departments. Each department has an individual policy statement for their folder’s write permissions.
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "ReadAllFolders",
      "Effect": "Allow",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::companybucket/*"
    },
    {
      "Sid": "WriteDepartment1Only",
      "Effect": "Allow",
      "Action": "s3:PutObject",
      "Resource": "arn:aws:s3:::companybucket/department1/*",
      "Condition": {
        "StringLike": {
          "aws:username": "*@department1.company.com"
        }
      }
    },
    {
      "Sid": "WriteDepartment2Only",
      "Effect": "Allow",
      "Action": "s3:PutObject",
      "Resource": "arn:aws:s3:::companybucket/department2/*",
      "Condition": {
        "StringLike": {
          "aws:username": "*@department2.company.com"
        }
      }
    },
    {
      "Sid": "WriteDepartment3Only",
      "Effect": "Allow",
      "Action": "s3:PutObject",
      "Resource": "arn:aws:s3:::companybucket/department3/*",
      "Condition": {
        "StringLike": {
          "aws:username": "*@department3.company.com"
        }
      }
    },
    {
      "Sid": "WriteDepartment4Only",
      "Effect": "Allow",
      "Action": "s3:PutObject",
      "Resource": "arn:aws:s3:::companybucket/department4/*",
      "Condition": {
        "StringLike": {
          "aws:username": "*@department4.company.com"
        }
      }
    },
    {
      "Sid": "WriteDepartment5Only",
      "Effect": "Allow",
      "Action": "s3:PutObject",
      "Resource": "arn:aws:s3:::companybucket/department5/*",
      "Condition": {
        "StringLike": {
          "aws:username": "*@department5.company.com"
        }
      }
    }
  ]
}
```
### **Q3:** OSI Security Architecture X.800 and AWS IAM
#### OSI Security Architecture X.800
The OSI Security Architecture X.800 standard outlines various security aspects to protect data and system resources, including:
- **Access Control**: Restricts unauthorized access to resources.
- **Authentication**: Confirms user identities.
- **Data Confidentiality**: Protects data from unauthorized access.
- **Data Integrity**: Ensures data has not been altered.
- **Non-repudiation**: Provides evidence of data exchange, preventing denial of participation.
- **Availability**: Ensures system and data availability when needed.
#### AWS IAM and X.800 Components
AWS IAM addresses several components of the X.800 standard:
- **Authentication**: Manages identity verification via access keys, passwords, and Multi-Factor Authentication (MFA).
- **Access Control**: Implements fine-grained access to resources through IAM policies.
- **Accountability**: Logs access and actions via AWS CloudTrail, supporting traceability and auditing.
- **Data Confidentiality (Indirect)**: Supports encryption permissions management for data security in AWS.
# Networking - Concepts
### Network
- **Definition**: A group of devices connected for data exchange.
- **Node**: Each device on the network, with a unique address.
### IP Address
- **Definition**: A numerical label for each device on a network using the Internet Protocol.
- **IPv4 Address**: Consists of 4 bytes (32 bits) separated by periods.
- **Example**: `192.168.1.10`
### IP Address Structure
- **Network Portion**: First R bits, identifies the network.
- **Host Portion**: Remaining H bits (32 - R), identifies the host.
- **Subnet Mask**: Defines values for R and H.
  - **Example**: `192.168.1.10` with subnet mask `255.255.255.0`
  - **Notation**: `192.168.1.10/24` (CIDR Notation)
### Subnetting and CIDR (Classless Inter-Domain Routing)
- **Subnet Mask**: Clusters IPs into subnets.
  - **Example**: `130.95.141.192` with subnet mask `255.255.255.192`
  - **CIDR Notation**: `130.95.141.192/26`
- **Calculating Hosts in a Subnet**:
  - Total IPs = 64; usable IPs = 62 (first and last are reserved).
  - **Network Address**: `130.95.141.192`
  - **Broadcast Address**: `130.95.141.255`
### CIDR (Classless Inter-Domain Routing)
- **Definition**: A notation to represent IP addresses with subnet masks.
- **Format**: IP address followed by a slash `/` and network portion bit length.
  - **Example**: `130.95.141.192/26`
### Summary
- **IP Address Composition**: Defined by network and host portions.
- **Subnet Mask**: Used for IP management and subnetting.
## Network
- A **network** is a group of connected devices for data exchange.
- Each device on the network is a **node** with a unique address.
## IP Address
- An **IP (Internet Protocol) address** is a numerical label for devices on a network using Internet Protocol.
- **IPv4 address**:
  - Contains 4 bytes (32 bits) separated by dots.
  - **Example**: `192.168.1.10`
## IPv4 Address Structure
- The first **R bits** represent the **network portion**.
- Remaining **H bits** (32 - R) represent the **host portion**.
- **Subnet mask** determines values for R and H.
  - **Example**: `192.168.1.10` with subnet mask `255.255.255.0`
  - **CIDR notation**: `192.168.1.10/24`
## CIDR Practice
- **CIDR Notation**: Combines IP address and subnet mask.
  - Example question: "Are `172.16.17.30/20` and `172.16.28.15/20` in the same subnet?"
- **Binary Conversion**:
  - IP addresses in binary highlight the network portion for subnet identification.
## Domain Name
- **Domain name**: Hierarchical naming structure.
  - Organized right to left.
  - **Example**: For `www.asad.javasoft.com`:
    - `.com` - top-level domain (TLD)
    - `javasoft` - second-level domain (SLD)
    - `www.asad` - subdomain
## DNS (Domain Name System)
- **DNS** translates mnemonic domain names to numeric IP addresses.
## Domain Name and URL
- **Domain name**: A human-readable structure of alphanumeric characters.
- **URL (Uniform Resource Locator)**:
  - Complete address to locate a specific resource.
  - **Components**: network protocol, domain name, path, and query parameters.
  - **Example**: `https://www.example.com/products/category?id=123&sort=asc`
## Port
- **IP Port**: Identifies a specific application protocol on a device.
- **Port Numbers**:
  - HTTP - 80
  - HTTPS - 443
  - SSH - 22
## Protocol
- A set of rules governing data transmission.
- **Examples**: HTTP, TCP, IP
- Protocols follow a **layered model**.
  - **TCP/IP**: Real-world model.
  - **OSI**: Conceptual model.
## OSI Model vs TCP/IP Models
- **OSI Model**:
  - 7 Layers: Application, Presentation, Session, Transport, Network, Data Link, Physical
- **TCP/IP Original**:
  - 4 Layers: Application, Transport, Internet, Link
- **TCP/IP Updated**:
  - 5 Layers: Application, Transport, Network, Data Link, Physical
  
![Pasted image 20241029090644.png](Cloud%20Computing%20%20Exam%20Notes-media/aafb231545074637ecf958eb1afd39a5b6818c52.png "wikilink")

- Question: **What is the difference between OSI and TCP/IP models?**
  - **OSI** has 7 layers with distinct Presentation and Session layers.
  - **TCP/IP Original** combines these into a single **Application layer**.
## 5-layer TCP/IP Model Overview
1. **Application Layer**:
   - Provides services directly to applications.
   - Examples: **HTTP, HTTPS** for web browsing, **SSH** for remote access.
2. **Transport Layer**:
   - Manages end-to-end data transfer between applications.
   - Examples: **TCP** (reliable), **UDP** (fast, connectionless).
3. **Network Layer**:
   - Routes packets to their destination.
   - Examples: **IP**, **ICMP**.
4. **Data Link Layer**:
   - Facilitates node-to-node data transfer.
   - Uses MAC addresses for identification.
   - Examples: **Ethernet**, **Wi-Fi**.
5. **Physical Layer**:
   - Manages data transmission over physical media.
   - Examples: **Optical fibers**, **Wireless radio waves**.
## Data Transmission in TCP/IP Model
- **Encapsulation Process**:
  - Application data → Transport segment (TCP/UDP) → Network packet (IP) → Data Link frame (MAC) → Physical bits.
  - Each layer wraps data in a protocol-specific header before passing it to the next layer.
  
![Pasted image 20241029090741.png](Cloud%20Computing%20%20Exam%20Notes-media/5313880f935ee1876dbf83ee8d139679a1e9fef6.png "wikilink")

## Encapsulation/Decapsulation in TCP/IP
- **Encapsulation**: Adding headers at each layer to prepare data for transmission.
- **Decapsulation**: Removing headers at each layer to interpret data at the receiving end.
- **Explanation**: Data moves down the layers (encapsulation) at sender, transmitted as bits, then moves up (decapsulation) at receiver.

![Pasted image 20241029090825.png](Cloud%20Computing%20%20Exam%20Notes-media/dc2c4ebb28ea33d066f416d05ee7075374443937.png "wikilink")

- Question: **Explain data encapsulation and decapsulation in TCP/IP**.
  - Encapsulation: Adds protocol-specific headers as data descends the layers.
  - Decapsulation: Removes headers as data ascends the layers at the receiver.
# Networking - Elastic Load Balancing
## ELB (Elastic Load Balancing)
- ELB serves as the single point of contact for clients, distributing incoming requests across multiple target groups (e.g., EC2 instances, containers).
- **Listener**: Checks incoming network requests using a pre-configured protocol and port.
### Diagram: ELB Architecture

![Pasted image 20241029090921.png](Cloud%20Computing%20%20Exam%20Notes-media/eaa7084540d3b1571a9923860ce9d2d2b21bfd77.png "wikilink")

### Example: Path-based routing
- Rule 1: URL pattern `/public/home` routes requests to `PublicWebServer` target group.
  ```json
  [
    {
      "Field": "path-pattern",
      "PathPatternConfig": {
        "Values": ["/public/*"]
      }
    }
  ]
  ```
- Rule 2: URL pattern `/admin/settings` routes requests to `AdminConsole` target group.
  ```json
  [
    {
      "Field": "path-pattern",
      "PathPatternConfig": {
        "Values": ["/admin/*"]
      }
    }
  ]
  ```
### Benefits of ELB
- **Availability & Fault Tolerance**: Ensures web application is accessible and resilient.
- **Health Check**: Monitors compute resources to ensure responsiveness.
  - *Healthy resource*: Responsive and functioning as expected.
- **Scalability**: Supports horizontal scaling by adding more resources.
  - **Horizontal Scaling**: Adding more instances of a resource.
  - **Vertical Scaling**: Increasing power of an existing resource.
### Scheme
- **Internet-facing**: ALB has a public IP.
- **Internal**: ALB has a private IP.

![Pasted image 20241029091020.png](Cloud%20Computing%20%20Exam%20Notes-media/870f8f42d9cfaeadcc7f1bd687fce270e93a3c96.png "wikilink")

## IP Address Type
- **IPv4**: Commonly used in real-world.
  - **Issue**: Limited to 4.3 billion addresses (IPv4 exhaustion).
- **IPv6**: Solution to IPv4 exhaustion.
  - Supports a much larger address space (2^128 addresses).
  - Mitigation: Use NAT (Network Address Translation) for private IPv4 ranges.
## NAT and Private IP Address Range
- **NAT**: Maps multiple private IPs to a single public IP for internet access.
  - Allows internal devices to share a single public IP.
- **Private IP Range**: Reserved for internal communication; not routable on the internet.
  - **Ranges**:
    - `10.0.0.0` to `10.255.255.255` (CIDR: `10.0.0.0/8`)
    - `172.16.0.0` to `172.31.255.255` (CIDR: `172.16.0.0/12`)
    - `192.168.0.0` to `192.168.255.255` (CIDR: `192.168.0.0/16`)
### Diagram: How NAT Works

![Pasted image 20241029091148.png](Cloud%20Computing%20%20Exam%20Notes-media/f9b7111af183e1b5a77407240eccc2b0901b98ea.png "wikilink")

### Example: VPC Setup with NAT Gateway
- **Public Subnet**: Hosts `Web Server EC2` with Elastic IP for internet access.
- **Private Subnet**: Hosts `DB Server EC2` without direct internet access.

  ![Pasted image 20241029091225.png](Cloud%20Computing%20%20Exam%20Notes-media/b07c2e3cc9deb8ea943ce78921cd0fcc04b24c84.png "wikilink")

### Networking - Elastic Load Balancing Setup
#### 1. **Set up an ALB (Application Load Balancer)**
- **Steps to Setup**:
  - Go to **EC2 Dashboard** > **Load Balancers** > **Create Load Balancer** > **Create Application Load Balancer**.
    - **Basic Configuration**:
    - **Scheme**:
      - **Internet-facing**: Routes requests from the internet to targets with public IPs.
      - **Internal**: Routes requests to private IPs within the same VPC.
    - **IP Address Type**:
      - **IPv4** or **Dualstack** (supports both IPv4 and IPv6).

    ![Pasted image 20241029091821.png](Cloud%20Computing%20%20Exam%20Notes-media/863198743b1a8f544ee6342174f35d89bf3d142f.png "wikilink")
  
  - **Network Configuration**:
    - **VPC Selection**: Choose the VPC to route traffic within the specified subnets.
    - **Availability Zones**: Select at least two for high availability.

![Pasted image 20241029091916.png](Cloud%20Computing%20%20Exam%20Notes-media/7eea3f35dd535634cc758a6f08a4bbe12f81be85.png "wikilink")

#### 2. **VPC (Virtual Private Cloud)**
- **VPC Overview**:
  - Isolated network for AWS resources.
  - Can be divided into **subnets** (public or private).
  - When created, an IP address range in the form of a **CIDR block** is specified, eg. 10.0.0.0/16. Range determines the total pool of IP addresses available within the VPC.
- **Internet Gateway**:
  - Allows traffic to and from the internet.
- **Subnet**:
  - Logical segmentation within a VPC, tied to a single Availability Zone.
- Within VPC, **subnets** are created to segment network. Each subnet is assigned smaller CIDR block from VPC’s range, e.g. 10.0.1.0/24, providing IP addresses for EC2 instances or other resources. Designated as either **public** or **private**.
  - **Public Subnet**: Requires an internet gateway for internet traffic.
  - **Private Subnet**: No direct access to the internet.
**Question**: How does VPC relate to the internal scheme of ALB?
  - An **internal ALB** uses private IPs and routes within the VPC without exposing traffic to the internet.
#### 3. **Security Group**
- **Definition**: Acts as a firewall to control inbound and outbound traffic for the ALB.
- **Configuration**:
  - Select an existing security group or create a new one during setup.
  
    ![Pasted image 20241029092103.png](Cloud%20Computing%20%20Exam%20Notes-media/a89828cfea65f4d719301eb570dd3ca1cc8c6328.png "wikilink")
    
    ![Pasted image 20241029092115.png](Cloud%20Computing%20%20Exam%20Notes-media/6b457ff069bee148fbed894346899547c545eae9.png "wikilink")

#### 4. **Listeners and Routing**
- **Listener**: Monitors requests from clients based on a configured **protocol** and **port**.
  - Supported protocols for ALB: **HTTP** and **HTTPS**.
  - Ports: Range from **1-65535**.
- **Routing**: Can forward requests to specific **target groups** based on rules.
    - **Example**: 
    - HTTP request on port 80 directed to `CITS5503-lecture6-TG`.
  
    ![Pasted image 20241029092134.png](Cloud%20Computing%20%20Exam%20Notes-media/6d1263190916e795b20451dd36dde9df78f52bdd.png "wikilink")
  
#### 5. **Create Target Group**
- **Target Group**: Defines the destination for routed requests.
  - **Types**:
    - **Instances**: Targets specified by EC2 instance IDs.
    - **IP Addresses**: Targets specified by IP ranges, supports IPv6.
  - **Usage**: Used in conjunction with Auto Scaling for flexibility.
  
    ![Pasted image 20241029092154.png](Cloud%20Computing%20%20Exam%20Notes-media/d01ed22948a7d2b4986f325d44f3ce75873f32a3.png "wikilink")
  
    ![Pasted image 20241029092230.png](Cloud%20Computing%20%20Exam%20Notes-media/3f0d4ff4f02a65f85be5222e3b16cf0b2e5d6388.png "wikilink")
  
#### 6. **Register Targets**
- **Registering**:
  - After creating a target group, add targets (e.g., EC2 instances) for load balancing.
  - **Health Checks**: Verifies if targets are healthy to receive traffic.
  
    ![Pasted image 20241029092247.png](Cloud%20Computing%20%20Exam%20Notes-media/a1b462d8e385326ba56f6556e55504d326599b10.png "wikilink")

### Key Concepts Summary
- **Elastic Load Balancing (ELB)**:
  - Increases application availability by distributing traffic across multiple targets.
  - **Health Checks**: Ensures only healthy targets receive traffic.
  - **Scheme**:
  - **Internet-facing**: Exposes the ALB publicly.
  - **Internal**: Limits access within the VPC, enhancing security.
- **Security Group**:
  - Protects the load balancer by restricting unwanted traffic.
- **Listener and Routing**:
  - **Listener**: Manages incoming connections.
  - **Routing**: Directs connections to appropriate target groups.
### Important Questions and Explanations
1. **Horizontal vs. Vertical Scaling**:
   - **Horizontal Scaling**: Adding more instances to distribute load.
   - **Vertical Scaling**: Increasing resources (e.g., CPU/RAM) on a single instance.
  2. **VPC and Internal Scheme Relation**:
   - **Internal ALB** routes within VPC without exposing endpoints to the internet, essential for secure private networks.
### Networking - Assignment Questions
#### **Question 1: Reasons for Using ALB with a Django Application**
- **High fault-tolerance**
  - ALB distributes traffic to multiple targets across groups.
  - Ensures Django application remains healthy, improving resilience.
  - Example: ALB reroutes requests from failed instances to healthy instances.
- **High scalability**
  - ALB enables horizontal scaling for Django.
  - Additional instances can be added to handle increased traffic.
  - Example: ALB evenly distributes load to new instances during traffic spikes.
- **Good match for Django**
  - Django uses HTTP and HTTPS, which ALB is optimized to manage.
  - ALB routes traffic efficiently, fitting Django’s architecture.
**Configuration Details:**
  - **Listener**: Listens on port 80 (HTTP) or 443 (HTTPS) with SSL termination.
  - **Target Group**: Contains Django instances on port 8000.
    - Health checks on endpoints like `/health/` to monitor instance status.
    - Session stickiness optional, depending on application needs.
#### **Question 2: Security in AWS Networks**
**1. Virtual Private Cloud (VPC)**
  - **Role**: Primary network environment for resource isolation.
  - **Security Features**:
    - Enables IP range control and subnet isolation.
    - Supports additional security configurations, like Network ACLs (NACLs).
  - **Implication**: Without VPC, resources lack network-level isolation and control.
**2. Security Groups**
  - **Role**: Acts as a firewall for instances within a VPC.
  - **Security Features**:
    - Manages inbound/outbound traffic based on IP, port, and protocol.
    - Stateful: Traffic allowed in one direction allows corresponding return traffic.
  - **Implication**: Missing security groups would expose instances to unwanted access.
**Similarities**:
  - Both secure resources within VPC.
  - Control over inbound/outbound traffic.
**Differences**:
  - **Scope**: VPC manages the network environment, Security Groups handle instance-level access.
  - **Statefulness**: VPC is stateless, while Security Groups are stateful.
# AI - Neural Networks
### What is AI?
- **Artificial Intelligence (AI):** Making machines perform tasks that mimic human actions.
- **Machine Learning (ML):** Allows machines to extract knowledge from data and learn autonomously.
- **Deep Learning (DL):** Uses neural networks to mimic biological brain structures, enhancing automated AI model training.
### Training and Adaptation in Neural Networks
- **Input Types for Model Training:** Text, images, speech, tabular data, 3D signals.
- **Model Training:** Various algorithms like Support Vector Machine, Random Forest, Neural Networks.
- **Model Adaptation:** Output can be applied to tasks like question answering, sentiment analysis, information extraction, image captioning, object recognition, instruction following.

  ![Pasted image 20241029093220.png](Cloud%20Computing%20%20Exam%20Notes-media/aa74c9998bd443b4ef60fc5be2ca0d36608466c7.png "wikilink")

### Types of Machine Learning
1. **Supervised Learning (SL):**
   - Uses labeled data.
   - Model has predefined outputs and learns by minimizing error.
   - Example: Predicting house prices based on historical data.
2. **Unsupervised Learning (UL):**
   - Uses unlabeled data.
   - Model identifies patterns or clusters without predefined output.
   - Example: Customer segmentation based on purchasing behavior.
3. **Reinforced Learning (RL):**
   - Feedback-based approach, learning from environment via rewards or penalties.
   - Focuses on maximizing total reward over time.
   - Example: Training a game-playing AI that improves by maximizing points.

![Pasted image 20241029093301.png](Cloud%20Computing%20%20Exam%20Notes-media/a354f5d3f365a0570e2346ca2d3540c82db00327.png "wikilink")

### Neural Network Structure
- **Layers:**
  - **Input Layer:** Receives input data.
  - **Hidden Layers:** Perform calculations on data.
  - **Output Layer:** Produces the final result.
- **Connections:** Each node in one layer connects to nodes in the next layer, weighted based on the importance of the input features.

  ![Pasted image 20241029093321.png](Cloud%20Computing%20%20Exam%20Notes-media/bb5f9dc8658d8a3807757b4be7107adcf6b501d7.png "wikilink")

### Perceptron (Single Node Neural Network)
1. **Linear Transformation:** Calculates a weighted sum of inputs.
$$
   Formula:
\sum wx + b
$$
   - Example: Predicting if an email is spam based on keywords.
2. **Non-Linear Transformation (Activation Function):** Transforms the linear output into a non-linear output for complex problem-solving.
   - **Sigmoid Function:** Used for binary classification
$$
f(x) = \frac{1}{1 + e^{-x}}
$$

![Pasted image 20241029093727.png](Cloud%20Computing%20%20Exam%20Notes-media/3173bb80bf173539f07778c8ececd8425481fd9c.png "wikilink")

### Activation Functions in Neural Networks
- **Sigmoid:** Maps input between 0 and 1, commonly used for binary classification.
- **Tanh (Hyperbolic Tangent):** Maps input between -1 and 1, providing better gradients for hidden layers.
- **ReLU (Rectified Linear Unit):** Outputs zero for negative values and linear for positive values, preventing vanishing gradient problems in deep networks.

  ![Pasted image 20241029093809.png](Cloud%20Computing%20%20Exam%20Notes-media/a1eceee96d3df2f1ad1be61197b0a6eb5c452f2e.png "wikilink")

# AI - Backpropagation and Performance Metrics
## Backpropagation
- **Objective**: Minimize the cost function, representing global error.
- **Parameter Update**:
  - Parameters (weights \(w\) and biases \(b\)) are adjusted to minimize the cost function.
  - Achieved via **calculus**, computing cost function derivatives.

    ![Pasted image 20241029093958.png](Cloud%20Computing%20%20Exam%20Notes-media/ce73b2008ad1dfad9d9bb3f07a0c884dc6532ba6.png "wikilink")

  - **Explanation**:
    - Uses optimization algorithms (e.g., **gradient descent**) to adjust parameters iteratively.
    - Each iteration reduces the cost function until convergence.
## Loss and Cost Functions
- **Loss**:
  - Difference between the prediction and the actual value for an individual data instance.
$$
Example Loss Function: ( l(\hat{y}, y) = (\hat{y} - y)^2
$$
- **Cost**:
  - Aggregate of losses across all data instances.
$$
  Example Cost Function:  C(\theta) = \frac{1}{N} \sum_{i=1}^{N} (\hat{y}_i - y_i)^2
$$
- **Training Goal**:
  - Minimize **Cost** to improve model accuracy.
  
    ![Pasted image 20241029094103.png](Cloud%20Computing%20%20Exam%20Notes-media/bf49c827cd85e6195dbb760c02b138a95a8d1bc4.png "wikilink")

  - **Explanation**:
    - Input **X** is passed through the network to get a predicted output **Y_hat**.
    - **Loss** is calculated as the error between **Y_hat** and true output **Y**.
## Metrics for Monitoring Model Performance
### Classification Metrics
- **Accuracy**:
  - Proportion of correctly classified instances.
$$
 \text{Accuracy} = \frac{TP + TN}{TP + FP + FN + TN}
$$
- **Precision**:
  - Proportion of true positive predictions among all positive predictions.
  - "Out of all positive predictions, how many were correct?"
  $$\text{Precision} = \frac{TP}{TP + FP}$$
- **Recall**:
  - Proportion of true positive predictions among all actual positives.
  - "Out of all actual positives, how many were correctly identified?"
$$
\text{Recall} = \frac{TP}{TP + FN}
$$
- **F1 Score**:
  - Harmonic mean of precision and recall.
  - Balances both metrics.
$$
 \text{F1 Score} = 2 \times \frac{\text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}}
$$

![Pasted image 20241029094726.png](Cloud%20Computing%20%20Exam%20Notes-media/ca2e58546996ceb4e02c6c74e9ee90ba8853aaff.png "wikilink")
    
### Regression Metrics
- **Mean Absolute Error (MAE)**:
  - Measures average absolute difference between predicted and actual values.
$$
 MAE = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i| 
$$
- **Mean Squared Error (MSE)**:
  - Measures average squared difference, giving higher weight to larger errors.
$$
 MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
$$
- **Cross-Validation Scores**:
  - Assess model performance on multiple data subsets to prevent overfitting.

    ![Pasted image 20241029094830.png](Cloud%20Computing%20%20Exam%20Notes-media/71f2785304ee0eaf6fd97226456c4fb8aea94159.png "wikilink")

  - **Explanation**:
    - Dots are actual data points; the line is the learned function.

    - Errors (e) are the differences between actual values $y$ and predicted $\hat{y}$.
# AI - AWS Services
### Artificial Intelligence on AWS

![Pasted image 20241029101508.png](Cloud%20Computing%20%20Exam%20Notes-media/2f8bc88c809f2f631a02bae5bbd83af86b51ebd3.png "wikilink")

### AWS Inference-as-a-Service (IaaS) Models
- **Inference Models**: Pre-trained and deployed models by AWS; users query these models for predictions. 
  **Examples**:
  - **AWS Comprehend**
    - Analyzes text and documents.
    - Provides insights on entities, key phrases, languages, sentiments, etc.
  - **AWS Rekognition**
    - Recognizes objects, scenes, and faces in images and videos.
    - Supports text-in-image detection and more.
### Amazon SageMaker
- **Purpose**: Simplifies building, training, and deploying machine learning models.
- **Features**:
  - **Jupyter Notebooks in SageMaker Web UI**
    - Fully managed for executing code, visualizing data, and documentation.
    - Handles infrastructure for running code (machines, containers).
  - **Code-Only Interaction**
    - Interaction via AWS SDK for Python (Boto3) or SageMaker Python SDK.
    - Custom Docker containers can be used for dependencies, managed on SageMaker's infrastructure.
# AI - Machine Learning Pipeline Tasks
1. **Preparing your Environment**
   - **Hardware & Software Requirements**: Access to AWS resources (e.g., EC2, S3, EBS).
     - Elastic Inference: Adds GPU acceleration for EC2.
     - CloudWatch: For monitoring and logging.
   - **Libraries**: Install libraries using `pip`.
     - Data: NumPy, Pandas.
     - Visualization: Matplotlib, Seaborn.
     - ML: Scikit-learn, TensorFlow, PyTorch.
   - **Configuration**: Set AWS credentials and configure SageMaker session using `boto3`.
2. **Task Definition and Data Preparation**
   - **Task Definition**: Define the problem (classification, regression, etc.), domain (image, text).
   - **Data Collection**:
     - Gather relevant data sources (databases, APIs).
     - Ensure data quality (clean, accurate).
     - Collect sufficient data for robust modeling.
3. **Model Selection**
   - **Model Choice**: Select model based on data type.
     - CNNs: Images.
     - Sequence models (LSTM, RNN): Text.
     - Tree-based models (Random Forests): Tabular data.
   - **Cost Evaluation**: Consider model size and data volume for budget.
4. **Data Preprocessing**
   - **Missing Values**:
     - Removal: Exclude rows/columns with missing data.
     - Imputation: Substitute missing values.
   - **Standardization & Normalization**:
     - Standardization: Mean-centers data.
     - Normalization: Rescales to fixed range [0, 1].
   - **Format-Specific Processing**:
     - Text: Tokenization, stop-word removal.
     - Tabular: Encode categorical values.
5. **Training and Hyperparameterisation**
   - **Training Components**:
     - **Loss Function**: Measures prediction error.
     - **Optimizer**: Adjusts weights (e.g., Adam).
     - **Training Loop**: Iterates through data.
     - **Validation**: Checks performance on separate data.
   - **Hyperparameters**: Control learning.
     - **Batch Size**: Samples per update step.
     - **Learning Rate**: Update step size.
     - **Epochs**: Passes over dataset.
6. **Evaluation**
   - **Test Data**: Evaluate on separate dataset.
     - **Metrics**: Accuracy, Precision, Recall, F1.
     - **Loss Per Epoch**: Monitor model performance.
   - **Monitoring**: Ongoing evaluation during training.
   - **Debugging**: Check data/preprocessing if performance is poor.
7. **Deployment and Inference**
   - **Model Deployment**:
     - Make model available via endpoints.
     - Scale with traffic using AWS EC2.
   - **Inference**:
     - **Real-Time**: Instant predictions for immediate needs.
     - **Batch**: Processes large datasets in batches.
# AI - Transformer Models
#### Overview of Transformer Models
- **Definition**: Powerful neural network models that serve as the foundation for Large Language Models (LLMs).
- **Popular LLM Examples**: ChatGPT, Claude, Co-Pilot.
#### Architecture
- **Encoder-Decoder Architecture**: Utilizes two components.
  - **Encoder**: Transforms input sequences.
  - **Decoder**: Generates output based on encoded input.
- **Attention Mechanism**:
  - **Purpose**: Captures long-range dependencies and relationships in sequences.
  - **Example**: Translates "How are you?" into Spanish as "¿Cómo estás?"
#### Image: Transformer Architecture

![Pasted image 20241029102037.png](Cloud%20Computing%20%20Exam%20Notes-media/257da8046247fc224c5ed9a2c17c57f0e37e696f.png "wikilink")
    
#### Characteristics of LLMs
- **Large**: Trained on extensive datasets with vast parameters.
- **General Purpose**: Solves a wide range of problems.
- **Prompt-Based**: Interaction through user input queries.
- **Pre-trained and Fine-tuned**: Initially trained on large datasets, then fine-tuned for specific tasks.
#### Image: LLM Characteristics
  ![Pasted image 20241029102116.png](Cloud%20Computing%20%20Exam%20Notes-media/f3f65967c0717ca255a28ccbfb7c14d6132b7b86.png "wikilink")

#### Fine-Tuning
- **Purpose**: Further trains a pre-trained model on a new, related dataset.
- **Method**: Unfreezes specific layers to learn task-specific features while retaining general knowledge.
- **Effectiveness**: Works best with a large, closely related dataset.
#### Image: Fine-Tuning Process

  ![Pasted image 20241029102200.png](Cloud%20Computing%20%20Exam%20Notes-media/5859e4203e10ad3ea9fb33593140d93d5b960daa.png "wikilink")

  - **Annotations**:
    - *Self-supervised training*: Initial pre-training with large data, resource-intensive.
    - *Supervised training*: Fine-tuning with labeled data, less resource-intensive.
#### SageMaker Jumpstart for Fine-Tuning
- **Tool**: Simplifies fine-tuning of models like Google’s FLAN T5 Transformer Model.
- **Example Tasks**:
  - Translation, sentiment analysis, summarization, etc.
#### Image: SageMaker Jumpstart T5 Example

![Pasted image 20241029102252.png](Cloud%20Computing%20%20Exam%20Notes-media/5fcf9da50e52aed7b7b4a5f7628bcf183f65a710.png "wikilink")

# AI - Pitfalls and Interest Topics
### AI/ML Pitfalls
- **Overfitting**
  - Model fits too closely to training data; performs poorly on unseen data.
  - Common causes: noisy data, small dataset, overly complex model.
  - **Implication**: Leads to poor generalization in real-world applications.
  - **Underfitting**
  - Model fails to capture patterns in data; performs poorly on training and test data.
  - Common causes: too few parameters, overly simplistic model, insufficient training.
  - **Implication**: Model cannot accurately predict outcomes, even on training data.
  
    ![Pasted image 20241029102355.png](Cloud%20Computing%20%20Exam%20Notes-media/8f79318cd4347abbb628013f03337962467afdcd.png "wikilink")

- **Insufficient Data Preprocessing**
  - Not cleaning, transforming, or handling missing values properly.
  - Failing to address outliers, scaling, or irrelevant features.
  - **Implication**: Model captures noise or irrelevant patterns, leading to inaccuracies.
- **Inappropriate Model Selection**
  - Selecting a model that doesn’t align with data nature or problem complexity.
  - **Implication**: Can cause overfitting or underfitting, resulting in poor performance.
- **Overconfidence in Model Outcomes**
  - Blindly trusting model predictions without further validation.
  - **Example**: Image classifier incorrectly identifies images due to context (e.g., snow in background labeled as "wolf").
  - **Implication**: Can lead to serious errors in critical applications.
  
    ![Pasted image 20241029102450.png](Cloud%20Computing%20%20Exam%20Notes-media/6336cecce8627b8852f1dfc3d3f170ec5ca51a38.png "wikilink")

### Further Interest Topics
- **Model Interpretability**
  - Efforts focus on explaining AI models that often act as "black boxes."
  - **Implication**: Enhances transparency, allowing better trust and regulatory compliance.
- **Model Hosting and Scalability**
  - Cost-effective strategies for hosting and scaling as model usage grows.
  - Examples: Multi-model deployment, AWS AutoScaling, AWS DeepSpeed Inference.
  - **Implication**: Enables models to handle high traffic efficiently without performance degradation.
- **Beyond AWS**
  - Exploration of AI/ML services on other cloud platforms.
  - Examples: Google Cloud AI, Microsoft Azure AI, GitHub Copilot.
  - **Implication**: Broadens scope for model deployment and tool integration.
# AI - Assignment Questions
## Types of Machine Learning Models on AWS
1. **Binary Classification Model**
   - **Purpose**: Predicts a binary outcome (e.g., yes/no, spam/not spam).
   - **Algorithm Used**: Logistic Regression.
   - **Examples of Questions Answered**:
     - "Is this email spam or not?"
     - "Will the customer buy this product?"
2. **Multiclass Classification Model**
   - **Purpose**: Predicts one of several classes (e.g., book, movie, clothing).
   - **Algorithm Used**: Multinomial Logistic Regression.
   - **Examples of Questions Answered**:
     - "What type of product is this?"
     - "Is this movie a comedy, drama, or thriller?"
3. **Regression Model**
   - **Purpose**: Predicts a continuous value (e.g., price, temperature).
   - **Algorithm Used**: Linear Regression.
   - **Examples of Questions Answered**:
     - "What will the temperature be tomorrow?"
     - "How many units will this product sell?"
## Machine Learning Project Plan Tasks on AWS
1. **Preparing Your Environment**
   - **Hardware and Software Setup**:
     - Provision AWS resources like EC2 Instances, S3 Buckets, EBS.
     - Attach IAM roles and permissions.
     - Enable Amazon CloudWatch for monitoring.
   - **Install Required Libraries**:
     - `NumPy`, `Pandas` for data manipulation.
     - `Matplotlib`, `Seaborn` for visualization.
     - `Scikit-learn`, `TensorFlow`, `PyTorch` for ML/DL.
   - **Setup Configuration**:
     - Configure AWS credentials and region.
     - Set up SageMaker session with `boto3`.
2. **Task Definition and Data Preparation**
   - **Define the Problem**:
     - Identify business problem and type (classification/regression).
   - **Data Collection**:
     - Store data in Amazon S3.
     - Ensure data is clean, representative, and sufficient.
3. **Model Selection**
   - **Choose Model Type**:
     - Binary Classification, Multiclass Classification, or Regression.
   - **Evaluate Costs**:
     - Consider model size, data scale, and budget.
4. **Data Preprocessing**
   - **Handle Missing Values**:
     - Options: Remove or use imputation (mean, median, etc.).
   - **Standardization and Normalization**:
     - Standardize to zero mean and unit variance.
     - Normalize to [0,1] range.
   - **Format-Specific Processing**:
     - Text: Tokenization, stop-word removal.
     - Tabular: Encoding categorical data.
5. **Training and Hyperparameter Tuning**
   - **Model Training on SageMaker**:
     - Define loss function, choose optimizer (e.g., Adam).
     - Set up a training loop.
     - Use validation set for monitoring.
   - **Hyperparameters**:
     - Tune batch size, learning rate, epochs.
6. **Evaluation**
   - **Evaluate on Test Dataset**:
     - Run final evaluation on test data.
   - **Metrics**:
     - Classification: Accuracy, Precision, Recall, F1, AUC.
     - Regression: MAE, MSE.
   - **Monitoring**:
     - Use CloudWatch for tracking performance.
7. **Deployment and Inference**
   - **Model Deployment**:
     - Deploy model to SageMaker endpoint for real-time/batch.
     - Enable autoscaling for traffic management.
   - **Inference Types**:
     - Real-Time: Instant predictions.
     - Batch: Large volumes in non-real-time scenarios.
## Accuracy Measurement for Final Model
- **Classification Metrics**:
  - **Accuracy**: Percentage of correct predictions.
  - **Precision**: Correct positive predictions out of total positives.
  - **Recall**: Correctly identified positives.
  - **F1 Score**: Balance between precision and recall.
- **Regression Metrics**:
  - **Mean Absolute Error (MAE)**: Average difference between predicted and actual.
  - **Mean Squared Error (MSE)**: Penalizes larger errors.
- **Cross-Validation**:
  - Use in SageMaker notebooks to improve model robustness.
Here's a condensed Markdown note format based on the images you've provided. The notes are structured with placeholders for images and key ideas in bullet points, as well as implications of each concept.
# Web Application Architecture
- **Definition**: Organizes software components and their interactions.
- **Definition**: Layout showing interactions between software components (e.g., frontend and backend)  

  ![Pasted image 20241029103909.png](Cloud%20Computing%20%20Exam%20Notes-media/d67965cd377b34e3c6f31bee3d105d38fa384658.png "wikilink")

## 1-Tier Web Application Architecture
- **Description**: All software components are on a single machine.
  - **Implications if Misused**: Limits scalability, may slow down with increased user load.
- **Example**: Basic standalone desktop application.

  ![Pasted image 20241029103955.png](Cloud%20Computing%20%20Exam%20Notes-media/aa3881b5fbe53715b75a62ee3863d315404ed1da.png "wikilink")

## 2-Tier Web Application Architecture
- **Description**: Client sends requests directly to a server, which processes and returns the response.
  - **Implications if Misused**: Increased complexity if the system scales; tight coupling between client and database.
- **Example**: Small business app with a client interface and separate database.

  ![Pasted image 20241029104016.png](Cloud%20Computing%20%20Exam%20Notes-media/d4136496cf9f8ba6aa2c5025d6af4fcf6003f791.png "wikilink")

## 3-Tier Web Application Architecture
- **Tiers**:
  - **Client Tier / Presentation Layer**: User interface and interaction management.
  - **Business Logic Tier / Application Server**: Manages data handling and business logic.
  - **Database Tier / Database Server**: Manages data storage, queries, and updates.
  - **Implications if Misused**: May lead to inefficient data handling or bottlenecks if improperly managed.
- **Example**: Web application with a frontend, backend server for logic, and a separate database server.

  ![Pasted image 20241029104043.png](Cloud%20Computing%20%20Exam%20Notes-media/aba9699d0e249a074fd424be93a963e37ca05da3.png "wikilink")

## Complex Web Application Architecture
- **Layers**:
  - **Presentation Layer**: Displays data to the user.
  - **Application Layer**: Contains business logic and processes requests.
  - **Database Layer**: Manages data storage and retrieval.
  - **Additional Services**: Specialized tasks (e.g., caching, data warehousing).
  - **Implications if Misused**: Increased complexity and maintenance costs.
- **Example**: Enterprise-level applications with specific service requirements.
## Serverless Architecture
- **Example Platform**: AWS
- **Workflow**:
  - **Client/Mobile Client** → **AWS API Gateway** → **AWS Lambda Function** → **AWS IAM** → **AWS CloudWatch** → **AWS DynamoDB**
  - **Explanation**: 
    - Clients make requests via the API Gateway.
    - Lambda function executes code based on the request.
    - IAM manages access permissions.
    - CloudWatch monitors system activity.
    - DynamoDB stores data.
  - **Implications if Misused**: Can lead to security risks without proper IAM settings, and cost inefficiency with excessive function executions.

    ![Pasted image 20241029104233.png](Cloud%20Computing%20%20Exam%20Notes-media/82485d0c7c176f276d5963f81397c4b4614cbef4.png "wikilink")

# Web Application Design Patterns
- **Definition**: Code-level reusable solution for implementing components and their interactions.
## Model-View-Controller (MVC)
- **Model**: Manages application data by interacting with the database for retrieving, updating, and storing data.
- **View**: Provides templates for data presentation to the user, handling layout and visual presentation.
- **Controller**: Intermediates between Model and View, processes user inputs, retrieves data from Model, and selects appropriate View to display data. It controls application logic and data flow.
  - **Implications if Misused**: Incorrect division of responsibilities can lead to tightly coupled code, making maintenance and scalability difficult.
- **Example**: A student management system where:
  - Model retrieves and stores student data.
  - View displays student information.
  - Controller manages interactions between Model and View.

    ![Pasted image 20241029105913.png](Cloud%20Computing%20%20Exam%20Notes-media/f9d3aeb9998a4eed787dc3ceb0ee2eaf5d1fdd25.png "wikilink")

  - **Explanation of Diagram Steps**:
    1. **Request**: End user sends a request.
    2. **Fetch Student Data**: Controller requests data from Model.
    3. **Database Query**: Model retrieves data from the database.
    4. **Return Data**: Model sends data back to Controller.
    5. **Fetch Presentation**: Controller fetches the View for data display.
    6. **Display Data**: View renders data for user presentation.
    7. **Response**: User receives the response.
## Django Web App Framework
- **Definition**: An open-source web application framework written in Python.
- **Customization of MVC**: Django uses Model-View-Template (MVT) instead of MVC.
  - **Model (M)**: Manages data interaction.
  - **View (V)**: Manages component interaction.
  - **Template (T)**: Manages data visualization.
  - **Implications if Misused**: Incorrectly structured views or models can lead to redundant data processing or slow response times.
- **Real-World Django Applications**: Instagram, Spotify, YouTube.
# Django Web App Framework Components
## URL Resolving
- **Function**: Maps incoming requests to the correct view function.
  - **Example**: `/user/1` maps to `UserView(id=1)`.
  - **Implications if Misused**: Incorrect URL mappings can lead to errors or inaccessible pages.
### Code Example: `urls.py`
```python
from django.urls import path
from music import views

urlpatterns = [
    path('', views.home, name='home'),  # Home page URL
]
```
## View Component
- **Function**: Uses resolved arguments to interact with templates and models.
- **Implications if Misused**: Complex views can slow down response time.
### Code Example: `views.py`
```python
from django.shortcuts import render

# View for rendering home page
def home(request):
    return render(request, 'home.html')
```
## Model Component
- **Function**: Interacts with the database to retrieve and manage data.
- **Implications if Misused**: Poorly designed models can lead to data redundancy or inefficiency.
### Code Example: `models.py`
```python
from django.db import models

# Model for Artist with name and song fields
class Artist(models.Model):
    name = models.CharField(max_length=100)
    song = models.CharField(max_length=25)
```
## Template Component
- **Function**: Renders data passed from the view into HTML or other formats.
- **Implications if Misused**: Inefficient templates can increase load times.
### HTML Example
![image](https://github.com/user-attachments/assets/7f57d5cd-0417-4e4c-8c28-e97d1be893e8)




![Pasted image 20241029110126.png](Cloud%20Computing%20%20Exam%20Notes-media/b9f41638e3ed8161ea3189225f3765c9a253f7ec.png "wikilink")

### Django-based Web Application Flow
1. **User Request**: User requests a URL.
2. **URL Resolving**: URL is mapped to a view.
3. **View Logic**: View contains logic to retrieve data and connect to templates and models.
4. **Model Interaction**: Model retrieves data from the database.
5. **Template Rendering**: Template displays data for the user.
# Django Music App - 1. Project Setup
## Demo: Overall Steps to create a Django Web App (named "music")
1. **Create a Django project and a music app**: Initialize the project structure.
2. **Set up the music app**: Configure app-specific settings.
3. **Enable template rendering**: Set up templates for HTML rendering.
4. **Render templates with retrieved data**: Display data from the database in templates.
## Step 1: Create a Virtual Environment
### Command to Create a Virtual Environment
```bash
mkdir ~/cits5503_django
cd cits5503_django
python3 -m venv cits5503venv
source cits5503venv/bin/activate
```
- **Why use a virtual environment?**
  - **Isolation**: Keeps Python dependencies separate for each project.
  - **Ease of Deployment**: Requirements can be listed using `pip freeze > requirements.txt` and reinstalled with `pip install -r requirements.txt`.
- **Note**: `/opt/wwc/` path is unsuitable for deploying Django apps as it requires **root privileges**, which the app does not need.
## Step 2: Create a Django Project and App
### Commands to Install Django and Initialize Project and App
```bash
pip install django
django-admin startproject CITS5503
cd CITS5503
python3 manage.py startapp music
```
- **Difference Between Commands**:
  - `django-admin startproject CITS5503`: Creates a project folder with a nested directory containing settings and manage.py.
  - `django-admin startproject CITS5503 .`: Creates project files directly in the current directory.
## Step 3: Start the Django Application Server
### Commands to Start Server
```bash
python manage.py check  # Checks for issues
python manage.py runserver  # Starts server on default port 8000
```
- **Default Port**: 8000
- **Custom Port** (if 8000 is in use):
  ```bash
  python manage.py runserver 9000
  ```
  - **Example (nginx config)**:
    ```nginx
    proxy_pass http://127.0.0.1:8000;
    ```
## Step 4: Access the Server
- **Access URL**: Open a browser and go to `http://localhost:9000`
- **Admin Interface**: Access at `http://localhost:9000/admin/` for admin tasks.

  ![Pasted image 20241029110607.png](Cloud%20Computing%20%20Exam%20Notes-media/61b70bbf810c273f5a560b0877acf770e9ef761b.png "wikilink")

## Step 5: Create an Admin
1. **Run Migrations**: Apply initial migrations to set up database tables.
   ```bash
   python manage.py migrate  # Applies all migrations (admin, auth, contenttypes, sessions)
   ```
   - **Implications if Misused**: Skipping migrations can lead to missing tables and errors in the admin panel.

      ![Pasted image 20241029110711.png](Cloud%20Computing%20%20Exam%20Notes-media/62d2ce91202c06d127e3e29cd50ec7cafda006b8.png "wikilink")

2. **Check Database**: Verify database tables with SQLite.
   ```bash
   sqlite3 db.sqlite3  # Opens database in SQLite
   .tables  # Lists all tables
   ```
   - **Example Tables**: `auth_user`, `django_session`, `auth_group`

      ![Pasted image 20241029110739.png](Cloud%20Computing%20%20Exam%20Notes-media/13167f16278bddd44fc5a86d8dde60a0a079eadb.png "wikilink")

3. **Create Superuser**: Add an admin user to access Django’s admin interface.
   ```bash
   python manage.py createsuperuser  # Prompts for username, email, password
   ```
   - **Implications if Misused**: Not creating an admin limits access to the Django admin panel.
4. **Restart the Server**: Ensure server reflects any recent changes.
   ```bash
   python manage.py runserver
   ```

    ![Pasted image 20241029111000.png](Cloud%20Computing%20%20Exam%20Notes-media/406ae5715493e69b3e9e274027166ef162c92fb4.png "wikilink")


5. **Access Admin Panel**: Go to `http://localhost:9000/admin/` and log in with the superuser credentials.

    ![Pasted image 20241029110924.png](Cloud%20Computing%20%20Exam%20Notes-media/743411adca88d1b2e4bc2b4ae5ceb756aa10ac93.png "wikilink")

# Django Music App - 2. Setup Music App
## Step 1: Register the App
- **Add App to Installed Apps**:
  - Open `CITS5503/settings.py`.
  - Add the following line to `INSTALLED_APPS`:
    ```python
    'music.apps.MusicConfig',  # Registers the music app
    ```
  - **Implications if Misused**: If not registered, Django will not recognize the app, causing issues in routing and functionality.
### Code Example
```python
INSTALLED_APPS = [
    'django.contrib.admin',  # The admin site
    'django.contrib.auth',  # Authentication
    'django.contrib.contenttypes',  # Content types framework
    'django.contrib.sessions',  # Session management
    'django.contrib.messages',  # Messaging framework
    'django.contrib.staticfiles',  # Static file management
    'music.apps.MusicConfig',  # New music app
]
```
## Step 2: Update the URL Component in the Project
- **Define App URL**:
  - Open `CITS5503/urls.py`.
  - Import views from the music app.
  - Add URL pattern for the home view.
    ```python
    from django.urls import path
    from music import views  # added

    urlpatterns = [
        path('', views.home, name='home'),  # Sets home page URL
        path('admin/', admin.site.urls),
    ]
    ```
  - **Implications if Misused**: Incorrect URL patterns will prevent users from accessing app views.
## Step 3: Update the View Component in the App
- **Create Home View**:
  - Open `music/views.py`.
  - Define a simple view function to display a message.
    ```python
    from django.shortcuts import render
    from django.http import HttpResponse  # added

    def home(request):
        return HttpResponse('This is the home page.')  # Displays text on home page
    ```
  - **Implications if Misused**: Missing or incorrect views result in "page not found" errors.
## Step 4: Access the App
- **Restart Server**: Restart the server to apply changes.
  ```bash
  python manage.py runserver 9000
  ```
- **Access URL**: Go to `http://localhost:9000` to view the home page message.

  ![Pasted image 20241029111147.png](Cloud%20Computing%20%20Exam%20Notes-media/b049ff79117a5c488512adc6f1e134982597dc54.png "wikilink")

# Django Music App - 3. Enable Rendering Template
## Step 1: Create HTML Templates in the Project and App
1. **Create Template Directories**:
   - Inside the current working directory of the project:
     ```bash
     mkdir templates
     mkdir music/templates
     mkdir music/templates/music
     ```
   - **Implications if Misused**: Missing directories will prevent Django from finding templates.
2. **Create HTML Files**:
   ```bash
   touch templates/home.html
   touch music/templates/music/main.html
   touch music/templates/music/artist.html
   ```
   - **Implications if Misused**: Missing HTML files result in rendering errors.
### Code Example for `templates/home.html`
```html
<h1>Home Page:</h1>
<ul>
  <li><a href="{% url 'home' %}">Home Page</a></li>
  <li><a href="{% url 'music:main' %}">Music Main Page</a></li>
  <li><a href="{% url 'music:artist' %}">Artist Page</a></li>
</ul>
```

![Pasted image 20241029111249.png](Cloud%20Computing%20%20Exam%20Notes-media/86735e68702cc22c8be3378ec1d8e5b0d777a90b.png "wikilink")

## Step 2: Update the URL Component in the Project
1. **Modify Main URL Configuration**:
   - Inside `CITS5503/urls.py`, add the URL pattern to include music app URLs.
   ```python
   from django.contrib import admin
   from django.urls import path, include
   from music import views

   urlpatterns = [
       path('', views.home, name='home'),
       path('admin/', admin.site.urls),
       path('music/', include('music.urls')),  # added
   ]
   ```
   - **Implications if Misused**: Incorrect URL configuration can lead to "page not found" errors.
## Step 3: Create the URL Component in the App
1. **Define App-Specific URLs**:
   - Create `music/urls.py` and define URL patterns for the app.
   ```python
   from django.urls import path
   from . import views

   app_name = 'music'
   urlpatterns = [
       path('', views.main, name='main'),  # Music main page
       path('artist/', views.artist, name='artist'),  # Artist page
   ]
   ```
   - **Question**: What kind of URL requests will be processed by the first URL pattern?
     - **Answer**: Requests to the `/music/` path will be processed, displaying the main page of the music app.

## Step 4: Update the View Component in the App

1. **Define View Functions**:
   - Inside `music/views.py`, define view functions to render templates.
   ```python
   from django.shortcuts import render

   def home(request):
       return render(request, 'home.html')  # Renders home page

   def main(request):
       return render(request, 'music/main.html')  # Renders music main page

   def artist(request):
       return render(request, 'music/artist.html')  # Renders artist page
   ```
   - **Implications if Misused**: Incorrect template names or paths will lead to template loading errors.
## Step 5: Register the Home Template in the Project
1. **Configure Template Directory**:
   - Open `CITS5503/settings.py`.
   - Update the `DIRS` setting in `TEMPLATES` to include the main templates directory.
   ```python
   import os  # added

   TEMPLATES = [
       {
           'DIRS': [os.path.join(BASE_DIR, 'templates')],  # added
           ...
       }
   ]
   ```
## Step 6: Restart the Server and Access the App
1. **Restart Server**:
   ```bash
   python manage.py runserver 9000
   ```
   - **Implications if Misused**: Failure to restart may prevent the application from recognizing new routes or templates.
2. **Access URLs**:
   - **Home Page**: `http://localhost:9000/`
   - **Music Main Page**: `http://localhost:9000/music/`
   - **Artist Page**: `http://localhost:9000/music/artist/`

      ![Pasted image 20241029111607.png](Cloud%20Computing%20%20Exam%20Notes-media/26ef314e7c22a8e8e6f9a6c422d7e1415ec15001.png "wikilink")

# Django Music App - 4. Rendered Templates with Retrieved Data
### Step 1: Add a Model in the App
- **Location**: `music/models.py`
- **Code**:
  ```python
  from django.db import models
  
  class Artist(models.Model):
      name = models.CharField(max_length=200)  # artist name
      song = models.CharField(max_length=200)  # artist song
      
      def __str__(self):
          return self.name  # returns artist name in string representation
  ```
- **Implication**: Defining models is essential as it provides the structure for database tables.
### Step 2: Create the Artist Table and Register it in the Admin Interface
- **Location**: `music/admin.py`
- **Code**:
  ```python
  from django.contrib import admin
  from .models import Artist
  
  admin.site.register(Artist)  # registers the Artist model with the admin site
  ```
- **Implication**: Registering the model allows it to be managed in the Django admin interface.
### Step 3: Make and Apply Database Migrations
- **Commands**:
  ```bash
  python manage.py makemigrations  # creates migration files
  python manage.py migrate         # applies migrations to the database
  ```
- **Output**: Confirms creation of `music_artist` table in the database.
- **Implication**: Skipping migrations will prevent the model from being reflected in the database.

  ![Pasted image 20241029111909.png](Cloud%20Computing%20%20Exam%20Notes-media/2f96348ebcedf8bfecb5ab871521be361eb4226a.png "wikilink")

### Step 4: Restart the Server and Access the Admin Interface
- **Action**: Open the Django admin interface at `http://localhost:9000/admin/`.
- **View**: Artists section is visible in the admin interface.
- **Implication**: Allows adding and managing `Artist` entries directly from the admin interface.
  ![Pasted image 20241029111932.png](Cloud%20Computing%20%20Exam%20Notes-media/eb85108e5294fd4f6775a1a624b4d09110e885b7.png "wikilink")

### Step 5: Populate the Artist Table
- **Action**: Use the admin interface to add artist entries, e.g., "Jerry" and "Tom."
- **Code** in `models.py`:
  ```python
  def __str__(self):
      return self.name  # displays the artist name in list views
  ```
  ![Pasted image 20241029111950.png](Cloud%20Computing%20%20Exam%20Notes-media/f72f690cfb88c4ff1f8bb8f3c6faf66ccdff49f9.png "wikilink")

### Step 6: Update the View Component in the App
- **Location**: `music/views.py`
- **Code**:
  ```python
  from django.shortcuts import render
  from .models import Artist
  
  def artist(request):
      title = 'Artist Page Info'  # page title
      artist_list = Artist.objects.all()  # retrieves all artist records
      context = {'title': title, 'artist_list': artist_list}
      return render(request, 'music/artist.html', context)  # sends data to template
  ```
- **Explanation**: Retrieves all artist entries and passes them to the `artist.html` template.
- **Implication**: Missing data retrieval or incorrect context keys will lead to display errors.
### Step 7: Update `music/templates/music/artist.html`
- **Code**:
  ```html
  <h1>{{title}}</h1>
  <ul>
      <li><a href="{% url 'home' %}">Home Page</a></li>
      <li><a href="{% url 'music:main' %}">Music Main Page</a></li>
  </ul>
  
  <ul>
      {% for artist in artist_list %}
          <li>{{artist.name}}: {{artist.song}}</li>
      {% endfor %}
  </ul>
  ```
- **Explanation**: Loops over `artist_list` to display each artist's name and song.
- **Implication**: Using incorrect variable names in the template will lead to undefined variable errors.
### Step 8: Restart the Server and Access the App
- **URL**: Access the artist page at `http://localhost:9000/music/artist/`.
- **Output**: Displays a list of artists and their songs.


  ![Pasted image 20241029112030.png](Cloud%20Computing%20%20Exam%20Notes-media/67a8985c12a21ab16923875f04d2998e702d0541.png "wikilink")

### Question: What if 'title' in Context is Replaced by 'titlectx'?
- **Original Code**:
  ```python
def artist(request):  
  title = 'Artist Page Info'
  artist_list = Artist.objects.all()
  context = {'title': title, 'artist_list': artist_list}
  return render(request, 'music/artist.html', context)
  ```
- **Modified Code**:
  ```python
def artist(request):  
  title = 'Artist Page Info'
  artist_list = Artist.objects.all()
  context = {'titlectx': title, 'artist_list': artist_list}
  return render(request, 'music/artist.html', context)
  ```
- **Template Change**:
```html
<h1>{{titlectx}}</h1>  <!-- updated to match context key -->
<ul>  
<li><a href="{% url 'home' %}">Home Page</a></li>  
<li><a href="{% url 'music:main' %}">Music Main Page</a></li>  
</ul>

<ul>

  {% for artist in artist_list %}  
  <li> {{artist.name}}: {{artist.song}}</li>

  {% endfor %}  
</ul> 
```
- **Implication**: Failure to match context keys between view and template results in missing data on the page.

# Web App/Architecture/Django Assignment Question
## Three Ways to Implement Microservice Architecture on AWS
1. **Using AWS Lambda with API Gateway (Serverless Microservices)**
   - Deploy independent functions as microservices, triggered by HTTP requests through API Gateway.
   - **Benefits**: Auto-scaling, reduced operational overhead, and cost efficiency as you only pay for usage.  
2. **Using Amazon ECS/EKS (Containerized Microservices)**
   - Run microservices as Docker containers managed by ECS or EKS.
   - **Benefits**: Flexibility with libraries and runtime, easy scaling, and more control over resource allocation.
3. **Using AWS Elastic Beanstalk (Managed Application Deployment)**
   - Deploy each microservice as a separate application on Elastic Beanstalk.
   - **Benefits**: Simplifies deployment and management while automatically handling load balancing and scaling.
### Benefits of Microservices on AWS
- **Scalability**: Each microservice can scale independently based on demand.
- **Fault Isolation**: Isolates failures, so one service failure doesn’t impact others.
- **Independent Deployment**: Enables continuous deployment without affecting the entire application.
### Handling Authentication and Authorization
- **AWS IAM**: Use IAM roles and policies for secure access control between AWS services.
- **API Gateway Authentication**: Integrate API Gateway with Cognito or use API keys, Lambda authorizers, or IAM-based authentication.
- **AWS Cognito**: Provides user pools and identity pools to manage authentication and access for users, useful for both API Gateway and direct client access. 
This approach improves security by enforcing strict access control and separation of concerns across services.
## Serverless Architecture Microservice Explained
### Implementation with AWS Lambda
- **API Gateway**: Acts as the entry point for client requests, routing them to appropriate Lambda functions.
- **Lambda Functions**: Each Lambda function represents a microservice that handles specific business logic and scales automatically based on demand.
- **DynamoDB**: A NoSQL database used for data storage, allowing Lambda functions to remain stateless.
- **CloudWatch**: Provides monitoring and logging for Lambda function execution, offering visibility into performance and errors.
### Benefits of Using Lambda for Microservices
- **Scalability**: Automatically scales based on incoming requests.
- **Reduced Overhead**: No server management required, fully managed by AWS.
- **Cost Efficiency**: Operates on a pay-per-use model, charging only for compute time.
- **Decoupling**: Enables independent development, deployment, and scaling for each Lambda function.
### Authentication and Authorization
- **Amazon Cognito**: Manages user authentication and integrates with API Gateway.
- **API Gateway + IAM Policies**: Enforces authorization by checking user roles and permissions.
- **JWT Tokens**: Cognito issues JWTs for secure access; Lambda functions validate these tokens to ensure authorized requests.
# DevOps Overview
- **DevOps**: Combination of cultural philosophies, practices, and tools to deliver applications faster than traditional software development.

  ![Pasted image 20241029113824.png](Cloud%20Computing%20%20Exam%20Notes-media/18e1f74149a697f5a948a545dc63df17a534c42c.png "wikilink")

### DevOps Best Practices
1. **Microservices**: 
   - Application is divided into small, loosely-coupled services.
   - Each service runs in its own process and communicates via network.
   - **Benefit**: Enables flexibility and easier updates.
   - **Example**: AWS Lambda.
2. **Monitoring and Logging**:
   - Continuous tracking of application and infrastructure performance.
   - **Benefit**: Helps in identifying real-time issues.
   - **Example**: AWS CloudWatch.
3. **Continuous Integration (CI)**:
   - Developers integrate code into a shared repository frequently.
   - Automated builds and tests are triggered after each integration.
   - **Benefit**: Speeds up bug detection and improves productivity.
4. **Continuous Delivery (CD)**:
   - Builds on CI by deploying changes to testing environments.
   - Prepares code for deployment to production with minimal manual intervention.
   - **Benefit**: Reduces time to release new features.
5. **Continuous Deployment**:
   - Extends CD by automatically deploying to production upon passing tests.
   - **Benefit**: Enables faster updates for users.

      ![Pasted image 20241029114458.png](Cloud%20Computing%20%20Exam%20Notes-media/750f7587964cfe6c41effef476aed5b7d50efe8d.png "wikilink")

### The Software/Application Release Process
1. **Source Control**:
   - Use Version Control Systems (VCS) like Git for tracking and managing code changes.
2. **Run Build and Unit Tests**:
   - Automated tests ensure individual components work correctly.
   - Failures alert developers to potential issues before deployment.
3. **Deploy to Test Environment**:
   - Deploys to a staging area for testing in an environment similar to production.
   - Includes various tests like functional, integration, and workload tests.
4. **Deploy to Production Environment**:
   - Final deployment where the application is accessible to end-users.

      ![Pasted image 20241029114344.png](Cloud%20Computing%20%20Exam%20Notes-media/54b236043116122ffc5de98ed31d1c229db7025f.png "wikilink")

# Fabric and SSH
## Fabric: Automate Tasks in DevOps
- **Fabric** is a high-level Python library to execute shell commands remotely over SSH, yielding Python objects.
- **OpenSSH** is a widely-used SSH protocol version, available on Mac, Linux/Unix, and Windows.
### Usage of OpenSSH in Authentication
- OpenSSH is used for user/client authentication by generating a pair of cryptographic keys (public and private).
  - Public Key: Shared with the server.
  - Private Key: Kept secure on the client.
- 
- **Question:** How is OpenSSH used for user/client authentication?

  ![Pasted image 20241029120336.png](Cloud%20Computing%20%20Exam%20Notes-media/eef9d971522e794b656a8fcfa562d7dc627391eb.png "wikilink")

- **Explanation of Diagram**:
  1. Client initiates SSH connection.
  2. Server sends a random message to the client.
  3. Client encrypts this message using its private key.
  4. Client sends the encrypted message back to the server.
  5. Server decrypts using the client's public key.
  6. If messages match, authentication succeeds.
## Adding SSH Public Key to GitHub
1. **Check for Existing OpenSSH Key Pairs**:
   ```bash
   ls ~/.ssh
   ```
2. **Generate OpenSSH Keys (if not present)**:
   ```bash
   ssh-keygen -t rsa -b 4096 -C email@example.com
   ```
   - Private Key: `id_rsa`
   - Public Key: `id_rsa.pub`
3. **Add Public Key to GitHub**:
   - Go to GitHub settings under "SSH and GPG keys."


      ![Pasted image 20241029120356.png](Cloud%20Computing%20%20Exam%20Notes-media/9591608ca0ee66763fc563eb00f2e7f1ac061a74.png "wikilink")

## Configuring OpenSSH for Fabric
1. **Install Fabric**:
   ```bash
   pip install fabric
   ```
2. **Create a Config File** in `~/.ssh` with the following contents:
   ```text
   Host myFabric
   Hostname 3.26.156.206
   User ec2-user
   UserKnownHostsFile /dev/null  # Disables host file check, insecure
   StrictHostKeyChecking no       # Disables host key check, insecure
   PasswordAuthentication no
   IdentityFile ~/.ssh/myFabricKey.pem
   ```
- **Implications**:
  - `UserKnownHostsFile /dev/null` and `StrictHostKeyChecking no` disable host key checking, reducing security.
  - Justification: Disabling host checks skips server authentication.
## Server/Host Authentication in SSH
- **Key Pair**: Server generates a host key pair.
  - Host Public Key: Distributed to clients.
  - Host Private Key: Kept secure on the host.
- **Key Exchange**: Occurs when a client connects to a server for the first time.

  ![Pasted image 20241029120505.png](Cloud%20Computing%20%20Exam%20Notes-media/e416d01b98bd13a4b7f76f9eecd0dba9a8ffeef4.png "wikilink")

## Host Key Checking in SSH
- **Host Key Checking**:
  - The client verifies the server's host key against the `known_hosts` file.
  - If the key matches, the server is authenticated.

    ![Pasted image 20241029120520.png](Cloud%20Computing%20%20Exam%20Notes-media/92449c3f4cf2189a71e8d1a3d2c98e50cc3e4d20.png "wikilink")

## Fabric Common Functions
1. **Upload a Local File to Remote Server**:
   ```python
   c.put(localfile, remotefilepath)
   ```
2. **Run a Remote Command**:
   ```python
   c.run(command, otherargs)
   ```
3. **Run a Remote Command with `sudo`**:
   ```python
   c.sudo(command, otherargs)
   ```
- **Example Code**:
   ```python
   from fabric import Connection
   c = Connection('myFabric')
   ```
## `sudo` vs `su`
- **sudo** (Superuser Do): Allows running specific commands as a superuser.
- **su** (Switch User): Allows switching to another user account with a password.
 
  - **Example of `sudo`**:
    ```bash
    sudo vim /etc/sudoers
    ```
  - **Example of `su`**:
    ```bash
    su root
    ```
## `su` vs. `su -`
- **su**: Does not change the working directory.
- **su -**: Changes to the target user’s home directory.
## Enable Server/Host Authentication in SSH Config
- Update configuration to enforce host authentication:
  ```plaintext
  Host myFabric
  Hostname 3.26.156.206
  User ec2-user
  StrictHostKeyChecking yes
  PasswordAuthentication no
  IdentityFile ~/.ssh/myFabricKey.pem
  ```
  ![Pasted image 20241029121037.png](Cloud%20Computing%20%20Exam%20Notes-media/4f361288fff6aeefa1e845f057bb590232e17820.png "wikilink")

## fabfile.py
- **Purpose**: A Python script with tasks for Fabric.
- **@task Decorator**: Used to define Fabric tasks.
- **Example Code**:
  ```python
  from fabric import task

  @task
  def fileOps(c):
      if c.run('test -f ~/myFabricFile', warn=True).failed:
          c.put('myFabricFile.tgz', '/home/ec2-user')
      c.run('tar -C ~/ -xf /home/ec2-user/myFabricFile.tgz')

  @task
  def sudoOps(c):
      c.sudo('cat /etc/passwd')
  ```
- **Explanation**: `fileOps` checks for a file, uploads if missing, and extracts. `sudoOps` runs a command with sudo privileges.
## Executing fabfile.py
1. **Navigate to Directory**:
   - Run `ls -al fabfile.py` to ensure the script is present.
   2. **List Tasks**:
   - Command: `fab -l`
   3. **Run a Task**:
   - Example: `fab -H ec2-user@52.62.6.162 -i ~/.ssh/myFabricKey.pem sudoOps`

# AWS Lambda Provisioning
### What is AWS Lambda?
- **Lambda**: A microservice that allows code to run without provisioning or managing servers.
- **Key Features**:
  - **Automatic Scaling**: Adjusts compute resources based on workload.
  - **Server Management**: Manages infrastructure, allowing focus on code and business logic.
### Benefits of AWS Lambda
1. **Automatic Scaling**
   - Seamlessly scales up/down based on workload.
   - No manual intervention required.
2. **Server Management**
   - Abstracts server maintenance.
   - Enables developers to focus solely on code.
### Example Tasks Using AWS Lambda
- **Task 1**: A simple Lambda function.
- **Task 2**: Lambda function integrated with S3 for storage.
### Task 1: Provisioning Steps
#### Step 1: Open AWS Lambda Console
- Access the Lambda service in AWS Console.
#### Step 2: Select a Lambda Blueprint
- Choose a blueprint or create a new function.

  ![Pasted image 20241029121310.png](Cloud%20Computing%20%20Exam%20Notes-media/4c1abbf6daae883ebcb69501ee8dbd91719bdbc7.png "wikilink")

#### Step 3: Configure Basic Information
- **Blueprint Name**: Select a name (e.g., "Hello world function").
- **Function Name**: e.g., `Hello_CITS5503`.
- **Runtime**: Select language runtime (e.g., Python 3.7).
- **Execution Role**:
  - Create a new role or select an existing role with appropriate permissions.
    ![Pasted image 20241029121323.png](Cloud%20Computing%20%20Exam%20Notes-media/515b7b1867caa9c7007a01ab2998592fae5d9000.png "wikilink")
    
#### Step 4: Preconfigured Function Code
- Modify or use the pre-configured code template.
```python
import json

print("Loading function")

def lambda_handler(event, context):
    print("value1 = " + event['key1'])  # Access key1 value
    print("value2 = " + event['key2'])  # Access key2 value
    print("value3 = " + event['key3'])  # Access key3 value
    return event['key1']  # Returns first key value
```
### Configuring Events
#### Step 5: Configure an Event to Trigger the Code
- **Test Event**: Create a test event to simulate invocation.
##### Step 5.1: Event Creation
- **Event Name**: e.g., `HelloCITS5503Event`.
- **Event Type**: Private (default setting).

  ![Pasted image 20241029121401.png](Cloud%20Computing%20%20Exam%20Notes-media/0c1585c896a2173eed84e49f04891ffcce0ebd8a.png "wikilink")

#### Step 5.2: Configure Event Data
- **Event JSON Template**: Define key-value pairs for test data.
Example:
```json
{
  "key1": "Hello, CITS5503",
  "key2": "value2",
  "key3": "value3"
}
```
#### Step 6: Trigger Lambda Function via Event
- Use the **Test** button to trigger the Lambda function with configured event.
#### Step 7: Execution Results
- View logs and output in **Execution Results** panel.
- Logs display function execution, including:
  - Event data used.
  - Output of print statements.
  - Execution duration and memory usage.

    ![Pasted image 20241029121439.png](Cloud%20Computing%20%20Exam%20Notes-media/7a6bf28b8abc0fbe801485150248e5df3cdc5f46.png "wikilink")

### Implications of Misconfiguration
- **Incorrect Role Permissions**: Lambda function may fail to execute due to insufficient permissions.
- **Inaccurate Event Configuration**: Improper JSON structure may cause function errors or unexpected behavior.
# AWS Lambda Task 2: S3 Example

  ![Pasted image 20241029121613.png](Cloud%20Computing%20%20Exam%20Notes-media/4a56dfad7a12afa2fbc17e5a1086a1849480879a.png "wikilink")

#### Step 1: Create an S3 Bucket
- **Description**: Create a bucket in Amazon S3 for storing objects that will trigger the Lambda function.

  ![Pasted image 20241029121625.png](Cloud%20Computing%20%20Exam%20Notes-media/233ec7fc696daf4734894485891518d6588c0df5.png "wikilink")

#### Step 2: Create a Permissions Policy
- **Description**: Define permissions for logging and accessing S3.
- **Log Event**: Entry in the log (e.g., message or error).
- **Log Stream**: Sequence of log events from the same source.
- **Log Group**: Group of log streams with shared monitoring settings.
- **Policy JSON**:
  ```json
  {
      "Version": "2012-10-17",
      "Statement": [
          {
              "Effect": "Allow",
              "Action": [
                  "logs:PutLogEvents",
                  "logs:CreateLogGroup",
                  "logs:CreateLogStream"
              ],
              "Resource": "arn:aws:logs:*:*:*"
          },
          {
              "Effect": "Allow",
              "Action": [
                  "s3:GetObject"
              ],
              "Resource": "arn:aws:s3:::*/*"
          }
      ]
  }
  ```
#### Step 3: Create an IAM Role
- **Description**: Allow Lambda to assume a role to access S3 resources.
- **Types of Trusted Entities**:
  - **AWS Account**: Trusts another AWS account.
  - **Web Identity**: Uses external web identity provider for authentication.
  - **SAML 2.0 Federation**: Trusts corporate credentials (e.g., Microsoft Active Directory).
  - **Custom Trust Policy**: Defines custom trust relationships.

![Pasted image 20241029121735.png](Cloud%20Computing%20%20Exam%20Notes-media/579bb87091318c60ac9a6cd41078e89f62ac6bee.png "wikilink")

##### Step 3.1: Create an IAM Role

![Pasted image 20241029121826.png](Cloud%20Computing%20%20Exam%20Notes-media/55375fa7b2055b93251b07fa8a2b0749371b4c86.png "wikilink")

![Pasted image 20241029121851.png](Cloud%20Computing%20%20Exam%20Notes-media/347a33196222da11714b0debfc02978279608519.png "wikilink")

#### Step 4: Create Lambda Function

![Pasted image 20241029121938.png](Cloud%20Computing%20%20Exam%20Notes-media/6c91c78c18d3b4d7654a5d45e2679eedc818b54a.png "wikilink")

- **Step 4.1**: Define function details like runtime, architecture, and existing IAM role.

  ![Pasted image 20241029121954.png](Cloud%20Computing%20%20Exam%20Notes-media/b02cfa07900a855db291e8d62cef35fee582d62d.png "wikilink")

- **Step 4.2**: Create Lambda function code to process S3 events.
  ```python
  import json
  import urllib.parse
  import boto3

  print('Loading function')

  s3 = boto3.client('s3')

  def lambda_handler(event, context):
      # Print received event for debugging
      # print("Received event: " + json.dumps(event, indent=2))
      bucket = event['Records'][0]['s3']['bucket']['name']  # Get bucket name
      key = urllib.parse.unquote_plus(event['Records'][0]['s3']['object']['key'], encoding='utf-8')  # Get object key
      try:
          response = s3.get_object(Bucket=bucket, Key=key)
          print("CONTENT TYPE: " + response['ContentType'])  # Log content type
          return response['ContentType']
      except Exception as e:
          print(e)
          raise e
  ```
**Explanation:**
1. event['Records']: contains an array of records. A record corresponds to a specific event that triggered the lambda function.
2. event['Records'][0]: retrieves the first record in this array.
3. event['Records'][0]['s3']: contains information specific to an S3 event in the record.
4. event['Records'][0]['s3']['bucket']: contains information about the S3 bucket where the S3 event occurred.
5. event['Records'][0]['s3']['bucket']['name’]: retrieves the name field from the bucket.
6. event['Records'][0]['s3']['object']['key']: retrieves the S3 object key from the S3 object, encoded by utf-8.
7. urllib.parse.unquote_plus(): a function call that decodes an encoded URL string.
8. encoding='utf-8': specifies the character encoding to be used when decoding the object key.

**Step 4.3: Deploy the Lambda Function**
![Pasted image 20241029122333.png](Cloud%20Computing%20%20Exam%20Notes-media/f89c1bcee9d35f35e971fe28f7e0038f8108eb30.png "wikilink")

#### Step 5: Add S3 Trigger to Lambda Function
- **Description**: Add an S3 trigger to automatically execute the Lambda function when objects are created in the bucket.

![Pasted image 20241029122348.png](Cloud%20Computing%20%20Exam%20Notes-media/ab273d71723ef91e559ca7d8562809a4e7f06b55.png "wikilink")
![Pasted image 20241029122410.png](Cloud%20Computing%20%20Exam%20Notes-media/1d819d9bd43ac266395c5c414b914ad0c45b81bb.png "wikilink")

#### Step 6: Test the Function with the Trigger
- **Description**: Upload an object to the S3 bucket to test if the Lambda function is triggered.
- **CloudWatch Logs**: Use CloudWatch to verify Lambda execution and logs.
- **Expected Log Entry**:
![Pasted image 20241029122423.png](Cloud%20Computing%20%20Exam%20Notes-media/42c38af0fb4775d09e210cf3fb942117ebbc4eff.png "wikilink")
