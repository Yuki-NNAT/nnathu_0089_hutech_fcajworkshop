---
title: "Event 3"
date: 2026-07-07
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Event Report: “FCAJ COMMUNITY DAY – DATA DRIVEN, AI RISEN”

### Event Objectives

- Provide practical insights into the development of AI and its impact on business operations.
- Introduce the application of modern solutions such as Voice AI, DevOps automation, and AI in recruitment.
- Share methods for establishing secure connections between AI Agents and internal systems through the Model Context Protocol (MCP) on AWS.
- Create opportunities for students and technology professionals to connect and learn from industry experts.

### List of Speakers

- **Steve Tran** – CTO/Founder, CloudThinker
- **Trung Vu** – CEO, Revve AI
- **Nghi Danh** – AI Engineer, Renova Cloud
- **Kiet Tran** – AI Engineer, AWS Student Builder Group
- **Bao Phan & Nguyen Nguyen** – Cloud Engineers, Cloud Kinetics
- **Truong Tran & Anh Dang** – AI Solution Sales, Noventiq
- **Toan Nguyen** – AWS Security Builder

### Key Highlights

#### Changes in Career Orientation

The rapid development of AI is changing recruitment requirements in the information technology industry. Many entry-level tasks can now be automated, while companies increasingly prioritize candidates with practical experience and the ability to use AI to improve their work efficiency.

From the presentations, I realized that IT students should actively participate in practical projects, build products, and gain experience as early as possible. In addition to technical knowledge, the ability to use AI as a supporting tool is becoming an essential skill.

#### DevOps Automation and Cloud Infrastructure

The event introduced a DevOps AI Agent capable of helping engineers analyze system logs, understand infrastructure topology, and identify the root causes of incidents. In certain cases, this solution can reduce investigation time from several hours to only a few minutes.

However, the AI Agent only performs analysis and recommends possible solutions. Engineers must still verify its findings and make the final decision before implementing any changes that could affect the system.

#### Voice AI Solutions for Vietnamese

Another notable topic was the development of Voice AI for Vietnamese, which remains a low-resource language compared with many more widely used languages because of the limited quantity and diversity of available training data.

Instead of using a direct Speech-to-Speech model, the presented solution divides the process into three stages:

1. **Speech-to-Text:** Converts the user’s speech into text.
2. **LLM Processing:** Uses a Large Language Model to analyze the request and generate an appropriate response.
3. **Text-to-Speech:** Converts the text response into spoken audio.

This approach gives the system greater control over its output, supports the recognition of regional accents and voice characteristics, and makes it easier to integrate Tool Calling for external tasks.

#### Applications of AI in Human Resources

The event also presented the use of AI to support recruitment processes, particularly when processing large numbers of candidate profiles.

By connecting Amazon Q to enterprise platforms and data sources, the system can assist with CV analysis, job description generation, candidate competency comparisons, and salary expectation reports.

This solution reduces manual workload and enables human resources departments to assess candidates using more consistent criteria. However, AI-generated results must still be reviewed by humans to minimize errors and bias during recruitment.

#### Securing Private MCP Connections

When Amazon Q or an AI Agent needs to access an internal database, protecting the data and limiting exposure to the public Internet are essential requirements.

The proposed architecture places the MCP Server in a private subnet within an Amazon VPC. It can combine VPC Endpoints, access control policies, and certificates managed through AWS Certificate Manager to protect data during transmission.

This architecture reduces the exposure of internal services, restricts the scope of access, and improves data protection when AI Agents interact with enterprise systems.

### Knowledge and Lessons Learned

#### The Role of AI in the Workplace

Through the event, I realized that AI is not used only to replace manual tasks. It can also help people analyze data, identify problems, and generate recommendations more quickly.

The ability to use AI effectively will become an important professional advantage. However, humans must still review the results, assess the risks, and remain responsible for final decisions.

#### Security When Building AI Agents

When an AI Agent is granted access to databases, APIs, or internal tools, security must be considered from the initial design stage.

Data flows should be encrypted, access permissions should follow the principle of least privilege, and critical services should be placed within private networks. The system should also maintain activity logs for auditing and incident investigation.

#### Selecting an Appropriate AI Architecture

For systems involving multiple complex tasks, dividing the processing workflow among specialized Agents can give each component a clearer responsibility. This approach can improve testing, access control, and error identification.

However, a Multi-Agent architecture is not always necessary. The choice between Single-Agent and Multi-Agent architectures should depend on the complexity of the problem, operational costs, and the system’s actual requirements.

### Application to the AI Recipe Finder Project

Based on the knowledge gained from the event, several solutions could be considered for improving and expanding the **AI Recipe Finder** project:

- **Strengthening backend connection security:** The database could be placed in a private subnet and made accessible only to the backend through appropriate network rules. If MCP is integrated in the future, the MCP Server should also be isolated and granted only the necessary permissions.
- **Protecting user data:** Information such as dietary preferences, favorite recipes, and allergy history should be encrypted during transmission and accessible only to authorized components.
- **Supporting incident analysis:** A DevOps AI Agent could be tested to assist with log analysis when the backend or application features encounter problems, such as unresponsive APIs or recipe images failing to load.
- **Separating AI responsibilities:** Features such as recipe search, ingredient analysis, and nutritional consultation could be divided into specialized components if the processing workflow becomes more complex.
- **Expanding with Voice AI:** In the future, the system could support Vietnamese voice interaction through a Speech-to-Text → LLM → Text-to-Speech workflow. Users could ask for recipes or receive cooking instructions by voice without directly interacting with the screen.

### Experience at the Event

Participating in **“FCAJ COMMUNITY DAY – DATA DRIVEN, AI RISEN”** was a valuable experience that introduced me to many practical applications of AI in system operations, voice interaction, recruitment, and Cloud infrastructure security.

#### Experiencing Practical Demonstrations

The demonstrations helped me better understand how AI solutions are applied in real-world environments. Notable examples included a Voice Agent providing product information through a call center, a DevOps AI solution identifying the causes of system incidents, and Amazon Q analyzing and assessing candidate profiles.

Through these demonstrations, I realized that AI can assist with many tasks within a short period. However, its effectiveness still depends on data quality, the scope of its access permissions, and the mechanisms used to validate its results.

#### Key Takeaways

- The ability to use AI effectively is becoming an essential skill for information technology engineers.
- AI should be used as a tool for analysis and recommendation, while humans must verify the results and remain responsible for final decisions.
- Security should be considered from the initial design stage, particularly when AI Agents connect to internal data and services.
- AI access permissions should follow the principle of least privilege, and important activities should be logged for auditing purposes.
- Multi-Agent architecture is suitable for systems with multiple specialized tasks, but its benefits, complexity, and operational costs must be carefully evaluated.
- AI solutions require output validation, exception handling, and fallback mechanisms for cases in which the generated results do not meet system requirements.

#### Event Photos

![Event 3](/images/4-Event/Event3_1.jpg)
![Event 3](/images/4-Event/Event3_2.jpg)