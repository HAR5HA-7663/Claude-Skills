# Key Projects for Applications

Use these projects when answering "tell me about a project" questions. Match project to role type.

## For AI Automation Engineer Roles

### AgenticAI – Multi-Agent Newsletter Automation (Apr 2025)
Designed and deployed newsletter automation using n8n (no-code) and CrewAI + LangChain (code-first) with structured output parsing, benchmarking both across latency, reliability, and developer speed. Built multi-agent coordination with function calling, custom FastAPI backends, deployed on AWS Lambda for scalable event-driven execution. Achieved 70% reduction in manual workload.

### CRE Research Agent – AI-Powered Literature Review (Nov 2024 – Present)
Built automated literature review system using multi-step RAG pipeline: query expansion, retrieval, reranking, summarization, discovering ~20 relevant papers per query. Implemented LangGraph-style state machine orchestration with dual vector databases (Qdrant + pgvector), BM25 sparse retrieval, and BGE cross-encoder reranking. Integrated Semantic Scholar, ArXiv, and Crossref APIs.

### N8N Workflow Automation – Self-Hosted AI Platform (Sep 2024)
Built newsletter automation workflow with AI agents integrating SerpAPI for trending topic discovery and Tavily AI for research. Deployed self-hosted AI starter kit with Docker Compose, Qdrant vector database for semantic search, and Ollama (Llama 3.2) for local LLM inference. Designed end-to-end automated pipelines from topic discovery to structured content generation with zero manual intervention.

### AI Resume Builder (Resumade.in) – Multi-LLM Automation (Jun 2025 – Present)
Architected serverless automation pipeline using FastAPI + AWS Lambda with multi-LLM orchestration (GPT-4, Gemini, DeepSeek) and structured JSON output for intelligent resume generation. Built real-time web scraping + AI optimization pipelines, reducing manual resume tailoring effort by 80%. Deployed with 95%+ uptime, sub-2s PDF/Word generation.

## For ML/AI Roles

### Resume Optimizer (QLoRA Fine-tuning)
Fine-tuned Qwen3-4B using QLoRA (4-bit NF4) for resume optimization. Reduced GPU memory to 18-22GB while maintaining quality. Used Hugging Face, PEFT, and custom training pipelines.

### ML Sentiment Analysis Loop (MLOps)
Built end-to-end MLOps pipeline with 8 microservices on Kubernetes. Implemented model training, evaluation, deployment, and monitoring with Prometheus/Grafana. Full CI/CD with automated retraining.

### Traffic Flow Prediction (GNN)
Applied Graph Neural Networks to predict traffic patterns using real-world sensor data. Combined spatial-temporal modeling with attention mechanisms.

### Pneumonia Detection (Computer Vision)
Built CNN-based medical image classifier achieving 92% accuracy. Implemented proper train/val/test splits and model interpretability with Grad-CAM.

## For Backend/SDE Roles

### FieldFuze Backend (Go + AWS)
Built entire backend in Go with 60+ AWS Lambda functions. Integrated Stripe (payments), Twilio (SMS), DocuSign (contracts), QuickBooks (accounting). Serves enterprise clients including Ferrari and Boeing.

### Job Portal API (FastAPI + HATEOAS)
RESTful API with HATEOAS architecture using FastAPI. Implemented proper pagination, filtering, and hypermedia controls. PostgreSQL with SQLAlchemy ORM.

### Lambda Microservices Architecture
Designed and deployed 94 Lambda functions with proper API Gateway configuration, error handling, and monitoring.

## For DevOps/Platform Roles

### Telegram Toxicity Bot (Kubernetes)
Deployed ML-based content moderation bot on EKS. Implemented circuit breakers, autoscaling, and Prometheus monitoring. Full Terraform infrastructure as code.

### Online Learning Portal (CI/CD)
Built Jenkins pipelines for automated testing and deployment. Implemented blue-green deployments and rollback strategies.

## For Full Stack Roles

### FieldFuze Mobile (React Native)
Built React Native app with 104+ components. Implemented offline-first architecture, push notifications, and real-time sync.

### VSCode Portfolio (Next.js)
Personal portfolio styled as VS Code interface. Next.js with TypeScript, responsive design, and animations.

## Quick Match Guide
| Role Type | Lead With |
|-----------|-----------|
| AI Automation Engineer | AgenticAI (CrewAI/n8n), CRE Agent (RAG), N8N Workflow, Resumade.in |
| ML Engineer | Resume Optimizer (QLoRA), ML Sentiment Loop |
| Backend SDE | Lambda Microservices, Job Portal API |
| DevOps/SRE | Telegram Bot (K8s), ML Sentiment Loop |
| Full Stack | Lambda Microservices (Go + React Native) |
| AI/LLM | AgenticAI, CRE Agent (RAG), Resume Optimizer |
