---
name: resume-tailor
description: >
  Tailors Harsha Vardhan Yellela's HTML resumes to specific job descriptions.
  Use when the user provides a job description and asks to create a tailored resume,
  make a resume for a specific role, or asks to "do the same" for a new JD.
  Outputs a tailored HTML resume to resumes/html/temp.html (or named file).
  Also handles updating existing resumes (sde, ml, devops, ai_automation, java_fullstack, resume.html).
---

# Resume Tailor (FAANG 1-Page Standard)

## CRITICAL: Resume Rules (Non-Negotiable)

1. **1 page strictly** — NO page breaks, NO 2-page resumes
2. **2 experience entries ONLY** — GRA (Jan 2025-Dec 2025) + Infor (Apr 2022-Dec 2023)
3. **NO CDF, NO Build Fellowship, NO EPAM** — these are dropped from all resumes
4. **XYZ bullet format** — "Accomplished [X] as measured by [Y] by doing [Z]"
5. **NO bold/strong inside bullet text** — only in skill category labels
6. **2-3 projects max** with GitHub links, 2 bullets each
7. **Summary: 2 sentences, ~30 words** — mirror JD language, no bold
8. **Skills: 4-5 categories, ~20 items total** — only interviewable skills
9. **Education: degree + GPA only** — NO coursework bullets
10. **NO Achievements section**

## Required Reading Before Tailoring

Always read these files first:

- `/home/har5ha/Desktop/resume/references/personal_details.md` - education, experience, skills
- `/home/har5ha/Desktop/resume/references/projects.md` - full project list with descriptions
- `/home/har5ha/Desktop/resume/CLAUDE.md` - role-to-project mapping tables

## Workflow

### Step 1: Analyze the JD

Extract:
- **Role type**: ML/AI, SDE/Backend, DevOps, AI Automation, Full Stack, Java, etc.
- **Must-have skills**: technologies, tools, frameworks explicitly required
- **Key phrases**: exact language from the JD to mirror in the summary
- **Nice-to-haves**: bonus skills to include if Harsha has them

### Step 2: Select Projects (2-3 max)

| Variant | Project 1 | Project 2 | Project 3 (if space) |
|---------|-----------|-----------|---------------------|
| **SDE** | Lambda Microservices (94 functions) | FieldFuze Backend (Go, RBAC) | Job Portal REST API |
| **ML** | Resume Optimizer (QLoRA, 9.5/10) | ML Sentiment Loop (MLOps) | LuffyGPT (from scratch) |
| **DevOps** | ML Sentiment Loop (Terraform, ECS) | Online Learning Portal (Jenkins, K8s) | Lambda Microservices |
| **AI Automation** | AgenticAI (CrewAI, LangChain, n8n) | CRE Research Agent (RAG) | Lambda Microservices |
| **Java Full Stack** | Inventra (Java 21, Spring Boot 3.5) | Job Portal REST API | FieldFuze Backend |

### Step 3: Write the Summary

2 sentences, ~30 words, NO bold tags. Mirror JD verbs and nouns.
- BAD: "Experienced ML Engineer with Python skills"
- GOOD: "ML Engineer with experience fine-tuning LLMs (QLoRA/PEFT), building 8-microservice MLOps platforms, and deploying models on AWS SageMaker."

### Step 4: Write Experience (2 entries only)

#### GRA Title by Role Type

| Role Type | GRA Title |
|---|---|
| SDE/Backend | Software Engineer Research Assistant – Agentic AI |
| ML/AI | ML Engineer Research Assistant – Agentic AI |
| DevOps | Platform Engineer Research Assistant – Agentic AI |
| AI Automation | AI Automation Research Assistant – Agentic AI |
| Java Full Stack | Software Engineer Research Assistant – Agentic AI |

#### Infor Title: Always `SDE-1 (LN Technical Consultant)`

#### Bullet Rules (XYZ Format)

- One bullet = one achievement, one metric
- Lead with impact verb (Reduced, Delivered, Deployed, Automated, Cut, Architected)
- Every bullet has at least one number (%, count, time, scale)
- NO semicolons — if it has one, split into separate bullets
- NO bold/strong tags inside bullet text
- GRA: 4 bullets, Infor: 3 bullets

#### GRA Base Bullets (reframe per role):
1. Reduced manual research workflow time by 70% by designing multi-agent orchestration pipelines (CrewAI + LangChain) that automated literature review, data extraction, and report generation.
2. Deployed 3 persistent agent services on AWS EKS/Fargate with OpenSearch Serverless for semantic search across 10K+ documents with sub-second retrieval.
3. Cut infrastructure provisioning from 2 hours to 15 minutes by implementing Terraform IaC with GitHub Actions CI/CD for automated container deployments.
4. [Role-specific bullet — ML: fine-tuning SLMs, DevOps: monitoring/Prometheus, AI: n8n benchmarking, SDE: FastAPI/GraphQL APIs]

#### Infor Base Bullets (same across all):
1. Delivered REST API integrations for 3 enterprise clients (Ferrari, Boeing, Triumph) processing 500+ daily transactions through AWS Lambda with S3 event triggers and API Gateway.
2. Reduced batch processing failures from weekly to monthly by resolving 15+ pipeline defects across MySQL databases and distributed ERP systems through systematic root-cause analysis.
3. Cut deployment turnaround by 25% by containerizing business logic services with Docker and standardizing CI workflows across client environments.

### Step 5: Write Skills (4-5 categories)

~20 items total. Only list what Harsha can discuss for 5 minutes in an interview.

**DO NOT include:** Jira, Confluence, IntelliJ IDEA, VS Code, GitBash, "Agile/Scrum", Claude Code, GitHub Copilot, OpenAI Codex

### Step 6: Write Projects (2-3 entries, 2 bullets each)

- Include GitHub links in header
- NO bold in bullet text
- Each bullet should have at least one metric

### Step 7: Output

- Copy CSS verbatim from `/home/har5ha/Desktop/resume/resumes/html/sde_engineer.html`
- Write to `resumes/html/temp.html`
- Tell user the suggested PDF name

## CSS Reference (use exactly this)

```css
body { margin: 0.3in auto 0.3in auto; line-height: 1.08; max-width: 7.5in; }
h1 { font-size: 22pt; margin: 6px 0 2px 0; }
h2 { font-size: 12pt; margin: 8px 0 2px; }
.contact-info { margin: 0 0 4px 0; }
p { margin: 2px 0 4px 0; }
.entry { margin-bottom: 5px; }
.entry .header { font-size: 10.5pt; }
.entry .subheader { font-size: 10.5pt; margin-bottom: 1px; }
ul { padding-left: 18px; font-size: 10pt; }
ul li { margin-bottom: 1px; }
ul li:before { left: -13px; }
```

## Existing Resume Files

| File | Role |
|------|------|
| `resumes/html/sde_engineer.html` | SDE/Backend/Full Stack (flagship) |
| `resumes/html/ml_engineer.html` | ML/AI/Data Science |
| `resumes/html/devops_engineer.html` | DevOps/Platform/SRE |
| `resumes/html/ai_automation_engineer.html` | AI Automation/Agentic/Integration |
| `resumes/html/java_fullstack.html` | Java Full Stack |
| `resumes/html/test_automation_enginner.html` | QA/Test Automation |
| `resumes/html/temp.html` | Scratch pad for one-off tailored resumes |

## References

- `references/experience-angles.md` - Per-role bullet patterns for each experience entry
