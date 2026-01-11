# cloud-engineering-portifolio-AWS
Concentrating on the AWS (Amazon web Services) with hands on projects terraform experiments and cloud architecture demos.
## Overview

Cloud computing is the backbone of modern digital systems. It enables organizations to build, deploy, and scale applications without owning physical infrastructure. This document introduces cloud computing from an engineering perspective, answering the most important questions: what it is, why it exists, when to use it, when not to, who should adopt it, and how organizations transition in and out of the cloud.

![image alt](https://github.com/lippatrick/cloud-engineering-portifolio-AWS/blob/main/image_01.png?raw=true)

### What Is Cloud Computing?

Cloud computing is the on-demand delivery of IT resources—compute, storage, databases, networking, security, and software—over the internet with pay-as-you-go pricing.

Instead of provisioning physical servers and data centers, organizations consume cloud services from providers that operate large-scale global infrastructure. This is possible through the technology of Virtualization.

Key characteristics:

  On-demand self-service
  
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
