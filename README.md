# cloud-engineering-portifolio-AWS
Concentrating on the AWS (Amazon web Services) with hands on projects terraform experiments and cloud architecture demos.
## Overview

Cloud computing is the backbone of modern digital systems. It enables organizations to build, deploy, and scale applications without owning physical infrastructure. This document introduces cloud computing from an engineering perspective, answering the most important questions: what it is, why it exists, when to use it, when not to, who should adopt it, and how organizations transition in and out of the cloud.

![image alt](https://github.com/lippatrick/cloud-engineering-portifolio-AWS/blob/main/image_01.png?raw=true)

### What Is Cloud Computing?

Cloud computing is the on-demand delivery of IT resources—compute, storage, databases, networking, security, and software—over the internet with pay-as-you-go pricing.

Instead of provisioning physical servers and data centers, organizations consume cloud services from providers that operate large-scale global infrastructure. This is possible through the technology of Virtualization.

Key characteristics:
  ``On-demand self-service
  Broad network access
  Resource pooling
  Rapid elasticity and scalability
  Measured (usage-based) service

### Why Cloud Computing Exists

Cloud computing exists to solve fundamental limitations of traditional IT infrastructure:

High upfront capital costs, Slow provisioning cycles, Poor scalability, Complex disaster recovery, High operational overhead.

The cloud shifts IT from a capital expense (CapEx) model to an operational expense (OpEx) model, allowing organizations to focus on delivering value rather than managing hardware.


## Types of Cloud Computing (Simple Explanation)

Cloud computing comes in two main ways and  thatt is how the it's owned and shared (Deployment Models) & how much work the provider does for you (Service Models)

### 1. Deployment Models (Who owns the infrastructure and who shares it)

### Public Cloud

A public cloud is like renting an apartment in a large building. The building is owned by a company (the cloud provider). Many tenants (customers) share the same building. Everyone is isolated and secure, but the infrastructure is shared. Small business / startups use this.

Examples: Amazon Web Services (AWS), Microsoft Azure, Google Cloud Platform and others

### Private Cloud

A private cloud is like owning your own house, only one organization uses the infrastructure. It can be inside the company’s premises or hosted by a third party offering more control costs more to run. Big enterprises like Banks and financial institutions, Governments, Organizations with sensitive or regulated data who what full control, custom security or compliance with strict regulations.

### Hybrid Cloud

A hybrid cloud is like having both a house and a rented apartment. Some systems stay on-premises (private cloud) and others run in the public cloud. Both environments work together. They are best used by organizations moving slowly to the cloud, companies with legal or data location requirements etcs.

### Multi-Cloud

A multi-cloud approach is like renting apartments in different cities. A company uses more than one cloud provider at the same time where each provider is chosen for what it does best.

### 2. Service Models

(How much responsibility the cloud provider takes vs you). Think of this as how much work you want to do yourself.

Infrastructure as a Service (IaaS), IaaS is like renting an empty house where the provider gives you the building, electricity, and water. You decide how to furnish and live in it.
What you get: Virtual servers || Storage || Networks || Security inside the system
Who it’s for: System administrators || Cloud engineers || Organizations needing full control 

Platform as a Service (PaaS). PaaS is like renting a fully furnished apartment and the provider handles the building and furniture. You just bring your personal items and live.
What you get: Ready-to-use platforms || Managed databases || Application runtimes
What you manage: Your application code || Your data
Who it’s for: Developers || Teams that want to focus on building software, not infrastructure

Software as a Service (SaaS). SaaS is like staying in a hotel where everything is already set up. You just use the service.
What you get: Fully managed applications || Access through a browser or app

Eg. Email services, Customer relationship tools (CRM), Online collaboration tools
Who it’s for: For everyone

## Why Use Cloud Computing?

Organizations adopt cloud computing for scalability and elasticity, Faster time to market, High availability and resilience, Global reach, Built-in security and compliance options, Support for DevOps and automation, Innovation in AI, data, and analytics

## When to Use Cloud Computing

Cloud computing is best suited when, Workloads are variable or unpredictable, Applications require rapid scaling, Users are globally distributed, High availability is critical, Disaster recovery is required, Teams practice CI/CD and DevOps

When NOT to Use Cloud Computing

Cloud may not be ideal when Workloads are stable and predictable over long periods or Latency requirements are extremely strict, Regulatory or sovereignty restrictions prohibit cloud use, Skilled cloud engineers are unavailable, Costs are not actively monitored or optimized

## Cloud Trade-offs (Pros and Cons)
Advantages
    No hardware procurement
    Elastic scaling
    Pay-per-use pricing
    Built-in redundancy
    Rapid experimentation

Challenges
    Cost overruns if poorly managed
    Vendor lock-in risks
    Shared responsibility misunderstandings
    Increased architectural complexity

## Who Should Adopt Cloud Computing?

Startups and scale-ups || Enterprises undergoing digital transformation || NGOs and public sector institutions || Research and education institutions || Remote and distributed teams

## Can Organizations Leave the Cloud?

Yes. Organizations may exit or reduce cloud usage due to Cost optimization decisions, Regulatory changes, Performance requirements, Strategic shifts. This is known as 'cloud repatriation'. Successful exits require portable architectures, Avoidance of tight vendor lock-in, Clear data ownership strategies


# Amazon Web Services (AWS) – Core Scope and Concepts


![image alt](https://github.com/lippatrick/cloud-engineering-portifolio-AWS/blob/main/res-architecture.png?raw=true)


Amazon Web Services (AWS) is a comprehensive cloud computing platform that provides on-demand access to computing resources such as servers, storage, databases, networking, and security services. AWS allows organizations to build and run applications without owning physical infrastructure, using a pay-as-you-go model that supports scalability, flexibility, and global reach.

AWS is built on a global infrastructure composed of regions, availability zones, and edge locations. Regions are geographic locations, while availability zones are physically separate data centers within a region designed to isolate failures. This architecture enables high availability, fault tolerance, and disaster recovery, making it possible to design systems that remain operational even when individual components fail.

Compute services in AWS provide the processing power required to run applications. These services support multiple execution models, including virtual servers and serverless computing. Choosing the right compute approach depends on workload characteristics, scalability needs, and operational responsibility. AWS enables applications to scale automatically based on demand, ensuring efficient resource utilization and consistent performance.

Storage services in AWS handle data persistence with varying levels of performance, durability, and access patterns. AWS supports object storage for files and static content, block storage for operating systems and databases, and file storage for shared access scenarios. Understanding how to select and manage storage types is critical for balancing performance, reliability, and cost.

AWS offers managed database services that reduce the operational burden of maintaining traditional databases. These services support relational and non-relational data models and are designed for high availability, automated backups, and scalability. Selecting the appropriate database depends on application requirements such as consistency, performance, and data structure.

Networking in AWS enables secure and controlled communication between cloud resources and the internet. Virtual networks isolate workloads, while routing, gateways, and load balancing manage traffic flow and availability. Proper network design is essential for security, scalability, and performance in cloud environments.

Security in AWS operates under a shared responsibility model, where AWS secures the underlying infrastructure while customers are responsible for securing their applications, data, and access controls. Identity management, encryption, monitoring, and auditing are core components of a secure AWS environment. Security must be integrated into architecture and operations from the beginning rather than added later.

Monitoring and operational management are essential for maintaining reliable cloud systems. AWS provides tools for collecting metrics, logs, and audit records to help detect issues, analyze performance, and ensure compliance. Effective monitoring enables proactive problem resolution and supports continuous improvement of system reliability.

Cost management is a critical aspect of cloud adoption. AWS pricing is based on actual resource usage, which requires active monitoring and optimization to prevent unnecessary expenses. Proper cost governance ensures that cloud environments remain financially sustainable while still delivering performance and scalability.

Automation and Infrastructure as Code are foundational practices in modern AWS environments. Automating infrastructure provisioning and configuration improves consistency, reduces human error, and enables repeatable deployments. These practices support DevOps methodologies and allow teams to manage complex environments efficiently.

AWS architectures are designed with reliability and scalability in mind. Systems are built to expect failures and recover automatically through redundancy, scaling, and fault isolation. Applying these design principles ensures applications can handle growth, traffic spikes, and infrastructure failures without service disruption.

This portfolio focuses on understanding AWS from an architectural and operational perspective, emphasizing secure design, scalability, cost awareness, and best practices. The goal is to demonstrate strong cloud fundamentals that form the foundation for real-world AWS solutions, automation, and production-grade systems.

https://docs.aws.amazon.com/whitepapers/latest/aws-overview/what-is-cloud-computing.html?utm_source=chatgpt.com
https://aws.amazon.com/documentation-overview/?utm_source=chatgpt.com
