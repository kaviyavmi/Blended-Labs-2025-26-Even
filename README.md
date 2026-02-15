# Blended-Labs

# EXP 1 - Introduction to AWS Identity and Access Management (IAM)

## Author
**Name:**  V M KAVIYA 

**Reg No** 212224040154

**Course:** Introduction to Cloud Computing  

## Title
Introduction to AWS Identity and Access Management (IAM)


## Objective
The objective of this lab is to understand how AWS Identity and Access Management (IAM) controls authentication and authorization in AWS. The lab focuses on exploring IAM users and groups, analyzing attached policies, assigning users to appropriate groups based on organizational roles, and validating permissions by testing service access.


## Prerequisites
- Basic understanding of cloud computing concepts  
- AWS Academy Lab access  
- Web browser with internet connectivity  


## Tools Used
- AWS Management Console  
- AWS Identity and Access Management (IAM)  
- Amazon EC2  
- Amazon S3  


## Tasks Performed

### Task 1: Explore IAM Users and Groups
- Reviewed pre-created IAM users: user-1, user-2, user-3  
- Explored IAM groups: EC2-Admin, EC2-Support, S3-Support  
- Inspected managed and inline policies attached to groups  
**Screenshot:**
  
<img width="1622" height="872" alt="image" src="https://github.com/user-attachments/assets/8170a13f-edbd-4655-9935-ceb12b38f668" />


### Task 2: Add Users to Groups
- Added user-1 to the S3-Support group  
- Added user-2 to the EC2-Support group  
- Added user-3 to the EC2-Admin group  
**Screenshot:**  

<img width="1918" height="1021" alt="Screenshot 2026-02-14 203457" src="https://github.com/user-attachments/assets/f5b4ba6f-7e27-49ae-8211-0395eb99bbfd" />


### Task 3: Test IAM User Permissions
- Logged in using IAM sign-in URL  
- Verified S3 access for user-1  
- Verified EC2 read-only access for user-2  
- Verified EC2 administrative access for user-3  
**Screenshot:**  

<img width="1919" height="1034" alt="Screenshot 2026-02-14 203907" src="https://github.com/user-attachments/assets/b71cba85-5043-4323-9c72-ff50608c6f17" />



## Workflow
1. Accessed IAM console and reviewed users and groups.  
2. Inspected policy permissions attached to groups.  
3. Assigned users to groups based on their roles.  
4. Logged in as each IAM user using the sign-in URL.  
5. Validated permissions by accessing AWS services.  


## Learning Outcomes
- Understood the role of IAM in AWS security.  
- Learned how IAM users, groups, and policies interact.  
- Gained practical experience implementing role-based access control.  
- Verified permission enforcement through real-time service testing.  


## Result
This lab provided hands-on experience with AWS IAM by demonstrating how organizations manage secure access to cloud resources. Assigning users to groups with predefined policies simplified permission management and ensured role-based access control across AWS services.



# EXP 2: Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: KAVIYA V M
* **Register Number**: 212224040154
* **Date of Submission**: 15-02-2026

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)

Step-1:

I started the lab and logged into the Amazon Web Services Management Console in the N. Virginia (us-east-1) region.

Step-2:

I created a custom VPC using Amazon VPC, configured public and private subnets, and enabled an Internet Gateway and NAT Gateway to manage internet connectivity.

Step-3:

I added additional public and private subnets in a second Availability Zone and updated the route tables to ensure proper routing for both internet-facing and private traffic.

Step-4:

I created a Security Group named Web Security Group and configured it to allow HTTP (port 80) access from anywhere to enable web traffic.

Step-5:

I launched an EC2 instance using Amazon EC2 in the public subnet, enabled auto-assign public IP, attached the security group, and selected the required key pair.

Step-6:

I configured a user data script to automatically install Apache and deploy a web application, then verified the web server by accessing the instance’s public DNS in a browser.

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1919" height="1029" alt="Screenshot 2026-02-15 112007" src="https://github.com/user-attachments/assets/5d1adcaf-f43e-4337-b73e-94459194c1ba" />


### Screenshot 2: EC2 Instance Running

<img width="1919" height="1016" alt="Screenshot 2026-02-15 114612" src="https://github.com/user-attachments/assets/5a60c4d9-1c24-4eec-81c9-fac78a6218a4" />


### Screenshot 3: Web Server Output in Browser

<img width="1919" height="1089" alt="Screenshot 2026-02-15 114749" src="https://github.com/user-attachments/assets/146222f2-3cf9-4ec1-89bd-d76d7c1e2109" />


## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
