---
title: "Event 1"
date: 2026-07-07
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# EVENT REPORT: “AWS FIRST CLOUD AI JOURNEY COMMUNITY DAY”

### Event Objectives

- Provide updates on practical trends in Cloud Computing and the application of Generative AI (GenAI) in enterprise environments.
- Share practical experience in software architecture design, Multi-Agent system development, and network infrastructure security on AWS.
- Create opportunities for members of the IT community to connect, exchange knowledge, and identify the skills required of engineers in the AI era.

### List of Speakers

- **Nguyen Gia Hung** – Solutions Architect, AWS Vietnam; Founder of FCAJ
- **Tinh Truong** – Platform Engineer, GoTymeX
- **Anh Pham** – Cloud Consultant, G-AsiaPacific Vietnam
- **Thinh Nguyen** – DevOps Engineer, FCAJ
- **Uyen Le, Thao Nguyen, Mai Nguyen** – GenAI Engineers, VIB
- **Duc Dao** – Solutions Architect, Cloud Kinetics
- **Vy Lam** – Senior Business Systems Analyst, VPBank

### Key Highlights

#### Career Trends and the Mindset of IT Engineers

The rapid development of AI is reducing the cost and time required for software development, thereby increasing the demand for technology products. In this context, engineers need not only technical knowledge but also a clear understanding of business problems and actual user needs. Practical products that they have designed and deployed provide stronger evidence of their capabilities than theoretical knowledge alone.

#### Context Optimization in AI Systems

The quality of an AI response depends significantly on the context provided to the model. To reduce hallucinations, the system should supply specific and relevant information while limiting the context to what is necessary for the request.

Providing a large amount of unfiltered information may increase processing costs and cause the generated results to become less accurate or relevant.

#### Automation with Amazon Q and AI Agents

The event introduced several applications of AI assistants in office work and data analysis, including processing Excel files, creating BI dashboards, and automatically summarizing meetings.

Through the Model Context Protocol (MCP), AI systems can connect to different tools and data sources to support the automation of business workflows.

#### Network Architecture and Security with Amazon CloudFront

The presentation introduced a flat-rate pricing solution that helps organizations control expenses and reduce the risk of “bill shock” when traffic increases unexpectedly or the system experiences a DDoS attack.

In addition, the AWS Point of Presence network can distribute traffic and reduce the workload placed on the origin infrastructure. VPC Origin enables CloudFront to access application resources located in private subnets, reducing the need to expose backend services directly to the Internet and strengthening the overall security of the system.

#### Hackathon Experience and GenAI Product Development

One of the notable sessions presented UTM Morpo, a project developed within 36 hours using a Serverless architecture coordinated by three AI Agents to generate user interfaces.

Instead of requiring AI to regenerate the entire interface after every modification, the development team implemented a feature that allowed users to edit individual components and CSS directly. This approach reduced processing time, saved tokens, and limited the generation of unnecessary code.

From this experience, the team learned how to manage token limitations, control AI-generated source code, and prioritize core functionality instead of attempting to include too many ideas in a single product version.

#### Controlling the Consistency of LLM Outputs

The speakers explained the probabilistic nature of Large Language Models. Even when `Temperature = 0`, the output may still vary because of hardware-level computations and inference optimization mechanisms used by model providers.

To reduce the effects of this uncertainty, a system may apply solutions such as JSON mode, output validation, multiple inference runs for result selection, or self-hosted models when stricter control is required.

Downstream services should also be designed to handle cases where AI-generated data does not follow the expected format or fails to meet system requirements.

#### Designing Enterprise Multi-Agent Systems

The event introduced a Multi-Agent system in which several specialized AI Agents work together to assess the creditworthiness of startup companies. Each Agent performs a specific task and contributes to the final result.

In addition to processing efficiency, this architecture introduces important security and compliance requirements in enterprise environments. The main topics discussed included controlling MCP attack vectors, preventing Prompt Injection, implementing Audit Trails, and periodically rotating API keys.

### What I Learned

#### Business-Oriented Technical Thinking

Through the event, I realized that the development of a technology product should begin with a real-world problem and the actual needs of its users. A technical solution only creates value when it effectively addresses a specific problem.

Dividing a system into specialized Agents or focusing on a well-developed core function can be more effective than implementing many features that have not been adequately optimized.

#### Architecture and Information Security

I gained a clearer understanding of the role of Amazon CloudFront in content delivery, reducing the workload on origin infrastructure, and supporting application protection against unusual traffic.

Combining CloudFront with VPC Origin can reduce the direct exposure of backend services to the Internet, thereby contributing to a more secure system architecture.

#### AI Risk Management

LLMs operate based on probability, so their outputs may not always be accurate or consistent. Therefore, production AI systems require mechanisms for output validation, context limitation, error handling, and fallback processing.

Systems must also control token usage, validate response formats, and restrict the permissions granted to AI when connecting to external tools or data sources.

### Application to the AI Recipe Finder Project

The knowledge gained from the event can be applied to the **AI Recipe Finder** project in several ways:

- **Task separation:** The AI workflow can be divided into specialized components for ingredient analysis, recipe retrieval, and nutritional calculation. This separation gives each task a clear scope and makes errors easier to identify.
- **Content generation optimization:** When a user requests an ingredient change, the system can update only the related content instead of regenerating the entire recipe, reducing response time and token usage.
- **Output validation:** A low `Temperature`, JSON mode, and Schema validation can be used to ensure that fields such as recipe names, ingredients, and cooking instructions follow the required structure.
- **Context limitation:** Prompts should contain only necessary information, such as the user’s available ingredients, nutritional requirements, and search conditions. User input should also be validated to reduce Prompt Injection risks.
- **Backend protection:** CloudFront and VPC Origin can be considered to reduce the direct exposure of application services. The database should remain in a private subnet and accept connections only from authorized backend services through appropriate network rules.

### Experience at the Event

Participating in the **“AWS FIRST CLOUD AI JOURNEY COMMUNITY DAY”** was a valuable experience that gave me a broader understanding of how AWS services and Generative AI can be combined to build secure and reliable applications.

#### Learning from Experienced Speakers

Experts and engineers from AWS, VIB, GoTymeX, G-AsiaPacific, and Cloud Kinetics shared practical experience in designing, developing, and operating modern technology systems.

Through case studies such as the product created during a 36-hour Hackathon and the Multi-Agent credit assessment system, I gained a deeper understanding of how complex workflows can be divided into specialized tasks instead of relying entirely on a single AI model.

#### Gaining Practical Technical Knowledge

The event helped me better understand the probabilistic nature of LLMs, the causes of hallucinations, and the effects of settings such as Temperature and JSON mode on output consistency.

I also learned how Amazon CloudFront and VPC Origin can reduce the direct exposure of application infrastructure, control incoming traffic, and improve protection against attacks.

Furthermore, the sessions on Model Context Protocol helped me understand both its ability to connect AI with external tools and the associated security risks, including Prompt Injection and MCP attack vectors.

#### Key Takeaways

- Dividing an AI workflow into specialized components or Agents can improve scalability, testability, and error identification.
- AI-generated results should never be trusted without validation. Systems require output checks, exception handling, and fallback mechanisms.
- Product development should prioritize solving the core problem effectively before adding more features.
- Security should be considered from the initial design stage, especially when AI is granted access to external data, tools, or services.
- Sensitive information such as API keys must be securely stored, protected by appropriate access controls, and rotated periodically.

#### Event Photos

![Event 1](/images/4-Event/Event1.jpg)