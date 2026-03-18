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
This lab provided hands-on experience with AWS IAM by demonstrating how organizations manage secure access to cloud resources.
Assigning users to groups with predefined policies simplified permission management and ensured role-based access control across AWS services.

---





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

---

# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

* **Name**:  KAVIYA V M
* **Register Number**: 212224040154
* **Date of Submission**: 28-02-2025

---

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity
* Basic knowledge of Linux commands (optional)

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Key Pair
* Security Group
* SSH Client (PuTTY / Terminal)

---

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.

---

### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.

---

### Task 3: Configure Security Group

Configure a security group to allow inbound access:

* SSH (Port 22) from your IP address
* HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.

---

### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:

```
ssh -i "keyname.pem" ec2-user@<Public-IP>
```

---

### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

* Stop the instance
* Start the instance
* Reboot the instance

Observe the state changes of the instance.

---

### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.

---

### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.

---

## Workflow (Student Explanation)

(Write the steps you followed in your own words)

1.Launched a new EC2 instance named Web Server in the N. Virginia region using Amazon Linux 2023 AMI and t2.micro instance type.

2.Enabled termination protection and stop protection, configured a security group, and added a user data script to install and start an Apache web server.

3.Monitored the instance using status checks, CloudWatch metrics, and system logs to ensure it was running properly.

4.Modified the security group to allow HTTP (port 80) traffic and accessed the web server using the public IP address.

5.Resized the instance to t2.small, increased the EBS volume size, explored EC2 service quotas, tested stop protection, and finally stopped the instance.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List

<img width="1919" height="1089" alt="Screenshot 2026-02-28 083814" src="https://github.com/user-attachments/assets/318e0d57-019c-441c-a0dc-3998c4456c0d" />


### Screenshot 2: SSH Connection to Instance

<img width="1919" height="1093" alt="Screenshot 2026-02-28 085115" src="https://github.com/user-attachments/assets/d64a96ff-d7c5-421d-be95-d29052b33ed2" />


### Screenshot 3: Instance Monitoring / Status

<img width="1919" height="1106" alt="Screenshot 2026-02-28 090849" src="https://github.com/user-attachments/assets/dbfff821-e45f-404a-89b2-fc6e821a972e" />


## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.

---

# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**: KAVIYA V M
* **Register Number**: 212224040154
* **Date of Submission**: 09-03-2026

---

## Objective

The objective of this experiment is to understand how Amazon Elastic Block Store (EBS) provides persistent block-level storage for EC2 instances. This lab focuses on creating and attaching an EBS volume, formatting and mounting it on an EC2 instance, storing data, and verifying data persistence after instance reboot.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing EC2 instance (Amazon Linux 2 preferred)
* Basic knowledge of Linux commands

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Amazon EBS
* SSH Client (Terminal / PuTTY)

---

## Tasks Performed

### Task 1: Explore Amazon EBS

Explore the Amazon EBS service through the EC2 dashboard. Observe different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

---

### Task 2: Create an EBS Volume

Create a new EBS volume in the same Availability Zone as the EC2 instance. Choose an appropriate size and volume type.

---

### Task 3: Attach EBS Volume to EC2 Instance

Attach the created EBS volume to the running EC2 instance as an additional block device.

---

### Task 4: Format the EBS Volume

Connect to the EC2 instance using SSH and format the attached volume with a file system (for example, ext4).

---

### Task 5: Mount the EBS Volume

Mount the formatted volume to a directory in the EC2 instance (for example, /data or /mnt/ebs).

---

### Task 6: Store Data in EBS Volume

Create files and directories inside the mounted EBS volume and store sample data.

---

### Task 7: Verify Data Persistence

Reboot the EC2 instance and verify that the data stored in the EBS volume is still available after reboot.

---

## Workflow (Student Explanation)

1.Created an Amazon EBS volume

2.Attached the volume to an EC2 instance

3.Created a file system on the volume

4.Added a file to volume

5.Created a snapshot of volume

6.Created a new volume from the snapshot

7.Attached and mounted the new volume to the EC2 instance

---

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created

<img width="1918" height="903" alt="image" src="https://github.com/user-attachments/assets/355ef699-bb8b-4fb8-8512-9b9a7f5fe296" />


---

### Screenshot 2: EBS Volume Attached to EC2

<img width="1918" height="918" alt="image" src="https://github.com/user-attachments/assets/488ee3f6-fc87-400f-aa70-fc000b629341" />

---

### Screenshot 3: Mounted Volume with Data

<img width="1917" height="920" alt="image" src="https://github.com/user-attachments/assets/cd240f90-a613-4b1f-983d-198c52c154e0" />


---

## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.

---

# Lab 5 – Build a Database Server (AWS)

## Author

* **Name**: KAVIYA V M
* **Register Number**: 212224040154
* **Date of Submission**: 18-03-26

---

## Objective

The objective of this experiment is to understand how to deploy and configure a database server in AWS. This lab focuses on launching an EC2 instance, installing a database management system (DBMS), configuring basic database settings, creating a sample database, and validating connectivity to the database server.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing VPC and EC2 knowledge (from previous labs)
* Basic knowledge of Linux commands and SQL

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Security Groups
* SSH Client (Terminal / PuTTY)
* MySQL / MariaDB / PostgreSQL (any one)

---

## Tasks Performed

### Task 1: Launch EC2 Instance for Database Server

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type and configure key pair and security group.

---

### Task 2: Configure Security Group for Database Access

Modify the security group to allow:

* SSH (Port 22) for remote access
* Database port (e.g., MySQL – 3306 or PostgreSQL – 5432)

---

### Task 3: Connect to EC2 Instance

Connect to the EC2 instance using SSH from your local machine.

---

### Task 4: Install Database Server

Install a database server software such as MySQL, MariaDB, or PostgreSQL on the EC2 instance using package manager commands.

---

### Task 5: Start and Configure Database Service

Start the database service and configure basic settings such as root password and user privileges.

---

### Task 6: Create a Sample Database

Create a sample database and a table inside it. Insert a few records into the table.

---

### Task 7: Test Database Connectivity

Test the database server by connecting to it locally or remotely and performing basic SQL queries.

---

## Workflow (Student Explanation)

1.First, a security group named DB Security Group was created to allow the web server to connect to the database using port 3306 (MySQL).

2.A DB Subnet Group was created with subnets from two Availability Zones to allow the database to run in a Multi-AZ environment for high availability.

3.A MySQL RDS instance named lab-db was created with the database name lab, username main, and password lab-password.

4.The database was associated with the DB Security Group and the Lab VPC so that the web server can securely connect to the database.

5.The web application running on the EC2 server was opened using its IP address, and the RDS endpoint, database name, username, and password were entered to interact with the database.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Instance for Database Server

<img width="1913" height="923" alt="image" src="https://github.com/user-attachments/assets/304278d7-d59f-4fac-9b2e-361150e3a179" />


---

### Screenshot 2: Database Service Running

<img width="1918" height="916" alt="image" src="https://github.com/user-attachments/assets/06b0e5b8-16ad-481b-939f-8a61602acda8" />


---

### Screenshot 3: Sample Database and Table

<img width="1736" height="998" alt="image" src="https://github.com/user-attachments/assets/876b3bad-5de9-4501-9f40-ffebbdcb0a74" />


---

## Result

This experiment demonstrated how to build a database server in AWS using an EC2 instance. By installing and configuring a DBMS, creating a sample database, and testing connectivity, the fundamentals of hosting and managing a cloud-based database server were underst
