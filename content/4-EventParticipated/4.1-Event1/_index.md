---
title: "Event 1"
date: 2026-06-27
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# FCAJ Community Day – June 2026

**Time:** June 27, 2026

**Location:** Floor 26 & 36, Bitexco Financial Tower, Ho Chi Minh City (also livestreamed on YouTube).

**Role:** Participant

### Event objectives
- Career orientation & tech mindset: Share practical perspectives from Founders and Experts on self-development paths in the era of amplified AI.
- Update specialized AI Agent trends: Go deep into Multi-Agent solutions, Vietnamese Voice AI, DevOps AI Agents, and Amazon Q directly applied to Enterprise/BFSI environments.
- Practical architecture & security implementation: Guidelines on designing Serverless systems, optimizing workflows (SDLC/HR), and establishing secure Private connections for AI.

### Highlighted content

#### 1. Cloud infrastructure operation via Agentic Platform
- Speaker: Mr. Steve Tran (Founder & CEO at Cloud Thinker, former Solution Architect at AWS)
- Labor market status in the AI era:
  - Businesses halt mass hiring or tighten criteria for Fresher/Junior roles. Priority is given to Senior personnel who collaborate exceptionally well with AI tools.
  - However, operating Production infrastructure is critical. Every minute of system downtime causes major revenue losses, so AI cannot completely replace humans yet.
- Agentic platform solution (Cloud Thinker):
  - Incident Investigation: Reads logs and investigates root causes of incidents within minutes instead of taking hours of engineer time.
  - Code & Infra Review: Automatic quality control before deploying to Production to resolve the bottleneck in the Quality Control testing phase.
  - FinOps: Automates 100% of Cloud cost management and optimization since the AI understands both AWS architecture and financial business logic.
  - Security & Pen Testing: Transforms hacker mindsets (Whitehat/Blackhat) into automated tools that simulate attacks (Penetration Testing) and evaluate infrastructure security.
- Technical architecture:
  - Single Agent vs Multi-Agent: A Single Agent can handle over 95% of tasks but easily experiences context window dilution. Multi-Agent setups with Specialist Agents help reduce context size, lower token costs, speed up processing, and support RBAC (Role-Based Access Control).
  - Unlike general Chat/Coding tools that pose risks of accidental production operations, the system is designed with Multi-layer Approval to ensure safety.

#### 2. Deploying Voice AI for enterprise (Vietnamese practicality & banking environment)
- Speakers: Mr. Hieu Nghi (Renova Cloud), Mr. Kiet (AWS Student Community Builder), Mr. Trung Do (Founder & CEO at R AI, former YC Founder)
- Vietnamese Voice AI challenges: Vietnamese is a Low-Resource Language, so direct Speech-to-Speech models worldwide do not yet support it well.
- Enterprise standard 3-step Voice AI architecture:
  1. STT (Speech-to-Text): Converts the customer's input audio into text.
  2. LLM Agent + Tool Calling: Feeds text into LLM processing with business-oriented prompts. Automatically calls APIs (Tool Calling) for tasks like card locking, balance inquiry.
  3. TTS (Text-to-Speech): Converts the response text into natural voice output returned to the user.
- Handling practical problems in production (VPBank, VIP):
  - Real-time streaming: Continuously streams data in all 3 steps to reduce call latency.
  - Gender detection: Automatically detects male/female voice to address customers accurately as "Anh/Chi" (Mr./Ms.).
  - Interrupt mechanism & context understanding (VAD & Context): Prevents the AI from interrupting the customer when they pause to think (e.g., when reading a phone number) and promptly stops the AI when the customer responds.
  - Regional accents: Trains models with 10–20% of Central/North/South accent data to increase recognition accuracy.
  - Human-in-the-Loop: When the AI cannot handle a query or detects that the customer is angry, it automatically transfers (handover) the call smoothly to a call center agent.

#### 3. Monitoring automation & incident resolution with DevOps AI Agent
- Speakers: Mr. Nguyen Nguyen & Ms. Bao (Cloud Engineers at Cloud Kinetics)
- Problems of traditional DevOps workflows:
  - Scattered monitoring data (Fragmented Telemetry) in multiple places (CloudWatch, CloudTrail, Grafana).
  - Knowledge Gap and constant context switching prolong the Mean Time to Detect (MTTD) and Mean Time to Resolution (MTTR).
- 6 pillars of DevOps AI Agent:
  - Context Learning: Learns infrastructure via Agent Space and generates an architecture map (Topology).
  - Control: Transparently limits resource access rights based on Resource Tags.
  - Integration: Expands connectivity with databases/tools using MCP (Model Context Protocol).
  - Collaboration: Integrates communications via Slack, ServiceNow, Jira.
  - Convenience: Easily configured directly on the AWS Console.
  - Cost-Effective: Flexible pricing based on execution time (around $0.083/second).
- 4-step incident resolution workflow:
  1. Triage: Triggered by Alert/CloudWatch or direct chat.
  2. Investigation: Formulates hypotheses and verifies them based on Topology/Logs to perform Root Cause Analysis.
  3. Mitigation: Proposes execution playbooks (Prepare -> Validate -> Execute -> Post-validate). Does not execute automatically to guarantee safety first (Safety First).
  4. Improvement: Proposes system upgrade plans to prevent future incident recurrence.
- Real demo & enterprise results:
  - DDoS Attack Demo: Agent detects simulated 1,000 req/s DDoS attack on ECS/ALB, identifies 10 ECS Tasks causing traffic overflow, and provides Terminal commands to stop tasks and recover the app.
  - Case Studies: WGU University reduced MTTR by 77% (from 2 hours to 28 minutes); Zenchef reduced Misconfiguration detection time by 75%; KDDI Group shortened incident resolution times from weeks to days.

#### 4. Optimizing recruitment & HR management with Amazon Q (Quick)
- Speakers: Mr. Truong (Quen) & Ms. Minh Anh (Solution Shapers at Noventic)
- HR department challenges:
  - Manual CV screening is time-consuming (Time-to-hire takes 1–2 months), risking missing key talent.
  - Subjective candidate evaluation, lacking quantitative data standards across departments.
  - High data security risks when uploading internal CVs/information to public AI services.
- Integration power of Amazon Q (Quick):
  - Action Connectors: Deep integration with Microsoft (SharePoint, Outlook, OneDrive), Google Workspace (Gmail, Drive), S3, Relational DB, Jira, Salesforce, GitHub, and MCP.
  - Security Governance: Model runs entirely on AWS Bedrock secure environment (Nova, Claude) and complies with Local Zone.
- Live Demo HR scenario (Quick Desktop):
  - Custom Skill Creation: Imports Markdown files for AI to define the "HR Talent Review Assistant" skill, including screening steps and experience level evaluation.
  - Automated CV Screening & Scoring: Reads and OCRs batches of CVs (including PDFs/scans), automatically matching them against the Junior Cloud Engineer Job Description (JD).
  - Visual Reports: Exports detailed HTML reports categorizing candidates (Strong, Good, Low), analyzing strengths/weaknesses, recommending interview questions, and providing salary benchmarks.

#### 5. Private MCP Server security architecture for Amazon Q in enterprises
- Speakers: Mr. Toan Nguyen (AWS Security Builder) & Mr. Hieu Nghi (Renova Cloud)
- Enterprise security risks: When Amazon Q connects to internal MCP Server systems (Zalo, WhatsApp, internal DBs, AWS resources...), using Public Endpoints exposes systems to DDoS, Man-in-the-Middle, or data leak vulnerabilities.
- Private security architecture model:
  - Places the MCP Server completely in the Private Subnet of the VPC.
  - Uses VPC Connection / Interface Endpoints to create private internal connections with Amazon Q.
  - Integrates Internal ALB with TLS encryption certificates (AWS Certificate Manager - ACM) and Route 53 Private Hosted Zone / Resolver to resolve internal DNS domain names.
  - Keeps all data traffic closed inside AWS Cloud (Zero Public Exposure).
- Estimated infrastructure operating cost: The operating cost of the private infrastructure (Route 53 Resolver, ALB, EC2, Endpoints, Secrets Manager) is estimated at $250 – $350/month depending on data traffic.

### Outcomes and values gained
- Tech mindset with AI: AI is an capability "amplifier." In complex areas like Production infrastructure or recruitment, AI plays a supporting/assistant role, but humans (Human-in-the-loop) always retain final decision-making power.
- Practical AI architecture: Mastered specialist Multi-Agent architectures to optimize context windows, the standard 3-step architecture for Vietnamese Voice AI, the 4-step DevOps Agent workflow, and private MCP Server connection methods for absolute enterprise security.
- Cross-industry implementation: Saw the outstanding automation potential from applying AI to Cloud infrastructure operations, automated incident troubleshooting, and optimizing HR/Business processes in enterprises.

### Proof of Participation
<img src="/images/event1/event1.jpg">
