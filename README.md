# Cloud Migration Architecture

**A Cloud TPM's end-to-end framework for migrating on-premises infrastructure to AWS — covering network design, identity management, monitoring, and operational runbooks.**

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?style=flat-square&logo=amazonaws)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)
![Role](https://img.shields.io/badge/Role-Cloud%20TPM-blue?style=flat-square)

---

## Project Overview

This repository documents a structured cloud migration program moving legacy on-premises workloads to AWS. It reflects real-world TPM leadership across infrastructure planning, security architecture, stakeholder alignment, and operational readiness — ensuring zero unplanned downtime during cutover.

**Business Context:** The organization operated 80+ on-premises servers with aging hardware, rising maintenance costs, and limited disaster recovery capability. This migration program delivered a secure, scalable AWS environment while reducing infrastructure costs by 40% and improving system availability from 99.5% to 99.95%.

---

## Repository Structure

aws-cost-optimization-playbook/
|-- Diagrams/          # Architecture diagrams, network topology, migration flow visuals
|-- iam/               # IAM policies, role definitions, least-privilege access controls
|-- monitoring/        # CloudWatch configs, alerting rules, health check dashboards
|-- runbooks/          # Operational runbooks for migration, rollback, and incident response
|-- vpc/               # VPC design, subnet layout, security groups, NACLs
|-- README.md

---

## Migration Phases

| Phase | Description | Duration | Status |
|-------|-------------|----------|--------|
| Discovery & Assessment | Inventory on-prem workloads, dependencies, and performance baselines | 3 weeks | **Complete** |
| Architecture Design | VPC topology, IAM framework, security controls, and monitoring strategy | 2 weeks | **Complete** |
| Pilot Migration | Migrate 5 non-critical workloads to validate architecture and runbooks | 2 weeks | **Complete** |
| Full Migration | Phased cutover of all production workloads with rollback plans | 4 weeks | **Complete** |
| Optimization & Handoff | Performance tuning, cost optimization, and team enablement | 2 weeks | **Complete** |

---

## Key Results

| Metric | Before | After | Impact |
|--------|--------|-------|--------|
| Infrastructure Cost | $42K/month | $25K/month | **-40% reduction** |
| System Availability | 99.5% | 99.95% | **Near-zero downtime** |
| Disaster Recovery RTO | 24+ hours | < 1 hour | **Business continuity** |
| Security Posture | Manual audits quarterly | Automated continuous | **Real-time compliance** |
| Deployment Velocity | 2-week cycles | Daily releases | **5x faster delivery** |

---

## Domain Breakdown

### `/Diagrams` — Architecture & Migration Visuals
- AWS architecture diagrams (VPC, subnets, availability zones)
- Migration flow and cutover sequence diagrams
- Before/after topology comparisons
- Data flow and dependency mapping visuals

### `/iam` — Identity & Access Management
- IAM role and policy definitions following least-privilege principles
- Service-linked roles for EC2, RDS, S3, and Lambda
- Cross-account access policies for multi-account strategy
- MFA enforcement and password policy configurations

### `/monitoring` — Observability & Alerting
- CloudWatch dashboard configurations for compute, network, and storage
- Custom metric definitions and alarm thresholds
- SNS notification routing for critical alerts
- Health check scripts and availability monitoring

### `/runbooks` — Operational Procedures
- Step-by-step migration runbooks for each workload category
- Rollback procedures with decision criteria and escalation paths
- Incident response playbooks for post-migration issues
- Knowledge transfer documentation for operations team

### `/vpc` — Network Architecture
- Multi-AZ VPC design with public/private subnet segmentation
- Security group rules and NACL configurations
- NAT Gateway and Internet Gateway setup
- VPN/Direct Connect hybrid connectivity design

---

## Tools & Services

| Category | Tools |
|----------|-------|
| **AWS Services** | EC2, RDS, S3, VPC, IAM, CloudWatch, Route 53, CloudTrail |
| **Migration** | AWS Migration Hub, Application Discovery Service, DMS |
| **Infrastructure as Code** | Terraform, CloudFormation |
| **Monitoring** | CloudWatch, Datadog, PagerDuty |
| **Program Management** | Jira, Confluence, Lucidchart |

---

## TPM Lens — Program Management Perspective

This project demonstrates core Cloud TPM competencies:

- **Stakeholder Alignment:** Coordinated migration schedule across Engineering, DevOps, Security, and Business Operations with weekly executive readouts
- **Risk Management:** Maintained rollback plans for every migration wave — zero unplanned rollbacks executed across 80+ workloads
- **Dependency Mapping:** Built comprehensive workload dependency matrix ensuring correct migration sequencing and zero circular-dependency failures
- **Cutover Orchestration:** Led live cutover events with cross-functional war rooms, real-time monitoring, and pre-defined go/no-go criteria
- **Knowledge Transfer:** Created operational runbooks and conducted training sessions to ensure self-sufficiency post-migration

---

## Related Projects

| Project | Description |
|---------|-------------|
| [HIPAA Cloud Governance Framework](https://github.com/Ewuack/hipaa-cloud-governance-framework) | Compliance-as-code for regulated environments |
| [AWS Cost Optimization Playbook](https://github.com/Ewuack/aws-cost-optimization-playbook) | Strategic cost reduction across AWS infrastructure |
| [Cloud Incident Response Simulation](https://github.com/Ewuack/cloud-incident-response-simulation) | Security incident detection and response |
| [Cloud SDLC Pipeline](https://github.com/Ewuack/cloud-sdlc-pipeline) | CI/CD pipeline with security gates |

---

**Author:** Erick Guacamaya — Cloud Technical Program Manager
**LinkedIn:** [linkedin.com/in/erickguacamaya](https://linkedin.com/in/erickguacamaya) | **GitHub:** [github.com/Ewuack](https://github.com/Ewuack)
