Aws Ec2 Jenkins Deployment simple Portfolio Demo 

## Project/Demo Overview
This project demonstrates my practical skills in Amazon Web Services (AWS) by provisioning an EC2 instance, securely accessing 
it via the terminal (SSH), deploying Jenkins, and making it accessible through the instance’s public IP address. The goal of this portfolio project is to showcase foundational cloud computing concepts, infrastructure setup, IAM usage, and DevOps tooling in a real-world scenario.

### What is Amazon EC2?
Amazon Elastic Compute Cloud (EC2) is a core AWS service that provides resizable virtual servers (instances) in the cloud. 
These servers allow users to run applications without having to invest in physical hardware. EC2 gives you full control over the operating system,
storage, networking, and security of your virtual machine, making it ideal for hosting applications, running backend services, CI/CD tools,
and performing compute-intensive tasks.

### Why Use EC2?
EC2 is widely used because it offers: Scalability (Easily increase or decrease compute capacity as needed), Flexibility (Choose from multiple operating systems, instance sizes, and configurations)
Cost Control (Pay only for what you use, with options like On-Demand, Reserved, and Spot instances), Security (Integrated with AWS IAM, security groups, and key-pair authentication)
Global Availability (Deploy instances in multiple regions worldwide). Now, the beauty of it all, AWS offers all these and can take care of it all only at a pay-as-you-go, meaning,
you only pay for what you are using at a given time. 

### EC2 Instance Types
AWS EC2 provides different instance families optimized for specific workloads: AWS continues updating new or comin up with new EC2 types as the market demands. This mean
the types are not only fixed to these as below.

General Purpose (e.g., t2, t3, t3.micro): Balanced CPU, memory, and networking || Ideal for small applications, testing, and learning (used in this project).

Compute Optimized (e.g., c5): High-performance processors || Suitable for compute-intensive workloads.

Memory Optimized (e.g., r5): Designed for memory-heavy applications.

Storage Optimized (e.g., i3): High disk throughput and IOPS.


### AWS Regions and Availability Zones
Region: A geographical location where AWS has data centers (e.g., us-east-1, eu-west-1) && Availability Zone (AZ): An isolated data center within a region.

Benefits of regions and AZs: High availability and fault tolerance, Reduced latency by choosing regions closer to users, 
This project is deployed in a selected AWS region, demonstrating region-based resource management. Identity and Access Management (IAM) to manage permissions securely, AWS uses 
IAM (Identity and Access Management).
AWS managed policies (Full Access policies) are temporarily used to simplify learning and setup. This allows access to EC2, security groups, and networking resources.
In production environments, least privilege policies should always be applied instead of full access.

### Project Architecture

- IAM User with required permission
- EC2 Instance (Amazon Linux)
- Security Group allowing:
- SSH (Port 22)
- Jenkins (Port 8080)
- Jenkins installed and running on EC2
- Jenkins accessed via PubliProject Architecture

Implementation Steps
1. Create an EC2 Instance

Log in to AWS Management Console

Navigate to EC2 → Launch Instance

Choose Amazon Linux 2

Select t2.micro / t3.micro

Configure key pair for SSH access

![image alt](https://github.com/lippatrick/cloud-engineering-portifolio-AWS/blob/main/Projects/shoots/ec2/Screenshot%20from%202026-01-22%2011-04-07.png?raw=true)

![image alt](https://github.com/lippatrick/cloud-engineering-portifolio-AWS/blob/main/Projects/shoots/ec2/Screenshot%20from%202026-01-22%2011-05-10.png?raw=true)

![image alt]()

![image alt]()

![image alt]()

![image alt]()

![image alt]()

![image alt]()

Configure security group:

Allow SSH (22)

Allow HTTP/Jenkins (8080)

2. Access EC2 via Terminal
ssh -i your-key.pem ec2-user@<PUBLIC-IP>
3. Install Jenkins on EC2
sudo yum update -y
sudo wget -O /etc/yum.repos.d/jenkins.repo \
https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
sudo yum install java-11-amazon-corretto -y
sudo yum install jenkins -y
sudo systemctl start jenkins
sudo systemctl enable jenkins
4. Access Jenkins via Browser

Open a browser and navigate to:

http://<EC2-PUBLIC-IP>:8080

Retrieve the initial admin password:

sudo cat /var/lib/jenkins/secrets/initialAdminPassword
Outcome

Successfully deployed an EC2 instance on AWS

Accessed the instance securely via SSH

Installed and configured Jenkins

Accessed Jenkins through the public IP address

This project demonstrates my understanding of cloud infrastructure, IAM, Linux server management, and DevOps tooling.

### Skills Demonstrated

- Provisioned and configured AWS EC2 instances for hosting and deployment
- Managed AWS IAM users, roles, and policies to enforce least-privilege access
- Performed Linux server administration tasks and remote management via SSH
- Installed, configured, and ran Jenkins for CI/CD automation
- Configured cloud networking, including VPC concepts and Security Groups for secure access control
- Applied DevOps fundamentals such as automation, continuous integration, and deployment best practices

https://www.jenkins.io/doc/book/installing/linux/


