---
title: "Event 2"
date: 2026-07-07
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Event Report: “FIRST CLOUD JOURNEY COMMUNITY DAY”

### Event Objectives

- Introduce practical applications of AWS in Cloud computing, AI, cybersecurity, and real-time systems.
- Share knowledge about Docker, DevOps, WebSocket, GraphRAG, and Machine Learning.
- Help students develop technical skills, teamwork, and career orientation through practical experience.

### List of Speakers

- **Nguyen Quoc Bao** – Multiplayer applications using Godot and AWS WebSocket
- **Tran Trung Vinh** – System Administrator, Central Retail Group
- **Bao Huynh** – Junior Cloud Native Developer, Endava Vietnam; Founder and Head of ITea Lab
- **Le Hoang Gia Dai** – AWS WAF and Machine Learning-based intrusion detection
- **Viet Phat** – AI Student, Swinburne University of Technology
- **Truong Huy Phuoc** – Effective teamwork

### Key Highlights

#### Real-Time Applications with AWS WebSocket

The presentation introduced a multiplayer architecture using Godot, Amazon API Gateway WebSocket, AWS Lambda, and Amazon DynamoDB. WebSocket maintains real-time connections, Lambda processes application logic, and DynamoDB stores player connections and game states.

This Serverless architecture is suitable for turn-based applications. Systems requiring continuous and high-frequency synchronization may need dedicated services such as Amazon GameLift.

#### Cloud and DevOps Career Development

The speaker shared a career journey from IT Helpdesk to System Administrator and Cloud–DevOps. Important skills include Linux, networking, troubleshooting, monitoring, documentation, automation, Docker, CI/CD, and Infrastructure as Code.

The session emphasized that practical projects and a strong understanding of core technologies are more valuable than learning many tools without sufficient practice.

#### Containerization with Docker

Docker packages an application together with its dependencies, helping it operate consistently across development, testing, and production environments.

Containers are more lightweight than virtual machines because they share the host operating system. Docker is particularly useful for backend deployment, microservices, testing environments, and CI/CD pipelines.

#### AWS WAF and Machine Learning

AWS WAF helps protect web applications from SQL Injection, XSS, malicious bots, brute-force attempts, and abnormal request rates.

The presented solution combined AWS WAF with a Machine Learning-based Network Intrusion Detection System. AWS WAF filters known attacks, while Machine Learning analyzes traffic behavior to identify unusual patterns.

The presentation also highlighted the importance of data cleaning, class balancing, model evaluation, logging, and security monitoring.

#### GraphRAG with Amazon Bedrock and Neptune

GraphRAG represents information through entities and relationships, enabling AI systems to answer questions that require multi-step reasoning.

Amazon Bedrock can support document processing and embedding generation, while Amazon Neptune stores and queries the knowledge graph. GraphRAG is useful for complex data relationships but should only be adopted when conventional RAG cannot satisfy the system’s requirements.

#### Effective Teamwork

Successful projects require clear responsibilities, regular communication, transparent progress tracking, and early reporting of difficulties.

Collaboration tools can support task management and document sharing, but each team member must remain responsible for completing assigned work and coordinating with others.

### Knowledge and Lessons Learned

#### Selecting an Appropriate Architecture

Technology should be selected according to actual workload requirements. A Serverless WebSocket architecture is suitable for some real-time applications, while more demanding systems may require dedicated servers.

Similarly, GraphRAG should be used only when relationships between data entities provide clear value beyond conventional information retrieval.

#### Cloud and DevOps Mindset

Cloud and DevOps involve more than learning individual tools. They require automation, monitoring, documentation, version control, repeatable deployment processes, and collaboration between teams.

#### Layered Security and Data Quality

A single security mechanism cannot prevent every threat. Combining AWS WAF, behavioral analysis, logging, monitoring, and alerting provides stronger protection.

The performance of Machine Learning also depends heavily on data quality. Invalid values, incorrect labels, and class imbalance must be addressed before model training.

### Application to the AI Recipe Finder Project

The knowledge gained from the event can be applied to the **AI Recipe Finder** project in several ways:

- Package the FastAPI backend with Docker to ensure consistency between local and EC2 environments.
- Consider CI/CD to automate backend testing and deployment.
- Document database connections, environment variables, Nginx, and system service configurations.
- Use AWS WAF to protect public application endpoints from common web attacks.
- Monitor backend and infrastructure logs through Amazon CloudWatch.
- Consider GraphRAG if the system later needs to analyze complex relationships among recipes, ingredients, nutrients, and allergies.
- Maintain clear responsibilities among frontend, backend, database, and AI team members.

### Experience at the Event

Participating in the **First Cloud Journey Community Day** provided valuable knowledge about Cloud architecture, DevOps, Docker, artificial intelligence, cybersecurity, and teamwork.

#### Practical Demonstrations

The WebSocket demonstration showed how AWS services can support real-time applications. The AWS WAF and Machine Learning presentation explained how traditional security controls can work together with behavioral analysis.

The Docker and GraphRAG sessions also demonstrated practical solutions for application deployment and AI systems involving complex data relationships.

#### Key Takeaways

- Technology should be selected according to actual system requirements.
- Docker improves consistency across development and deployment environments.
- Cloud and DevOps require automation, monitoring, and documentation.
- Layered security is more effective than relying on one protection mechanism.
- Machine Learning performance depends strongly on data quality.
- Practical experience and effective teamwork are essential for project success.

#### Event Photos

![Event 2](/images/4-Event/Event2_1.jpg)
![Event 2](/images/4-Event/Event2_2.jpg)