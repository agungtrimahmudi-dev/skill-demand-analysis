# Learning Plan — Roadmap Menutupi Skill Gap
*Generated: 2026-08-10 03:19*

## 🎯 Prinsip
- **Project-based**: setiap skill dipelajari via proyek nyata (bukan tutorial saja)
- **Leverage existing**: build di atas stack Agung (n8n, Python, Docker, self-hosted)
- **Portfolio-first**: output = repo GitHub public dengan README, CI, tests, docs

## 📅 12-Week Sprint Plan
### Week 1-2: Kubernetes Fundamentals
- **Goal**: kind/k3d local cluster → deploy n8n + FastAPI via Helm
- **Repo**: `agungtrimahmudi-dev/k8s-learning-lab`
- **Deliverable**: Working demo + README + CI + tests ≥80% coverage

### Week 3-4: AWS Serverless
- **Goal**: Lambda + Step Functions workflow → replace 1 n8n flow
- **Repo**: `agungtrimahmudi-dev/aws-serverless-automation`
- **Deliverable**: Working demo + README + CI + tests ≥80% coverage

### Week 5-6: Next.js + TypeScript Full-Stack
- **Goal**: Dashboard monitoring n8n (App Router, Tailwind, TanStack)
- **Repo**: `agungtrimahmudi-dev/nextjs-ai-dashboard`
- **Deliverable**: Working demo + README + CI + tests ≥80% coverage

### Week 7-8: Vector DB Production
- **Goal**: Pinecone/Mongo Atlas Vector Search → migrate Recipe RAG
- **Repo**: `agungtrimahmudi-dev/vector-db-rag`
- **Deliverable**: Working demo + README + CI + tests ≥80% coverage

### Week 9-10: LangGraph Multi-Agent
- **Goal**: Research → Code → Review agent pipeline
- **Repo**: `agungtrimahmudi-dev/langgraph-agent`
- **Deliverable**: Working demo + README + CI + tests ≥80% coverage

### Week 11-12: Observability & IaC
- **Goal**: Prometheus/Grafana/Loki + Terraform modules
- **Repo**: `agungtrimahmudi-dev/observability-iac`
- **Deliverable**: Working demo + README + CI + tests ≥80% coverage

## ✅ Definition of Done per Sprint
1. Repo public di GitHub dengan `main` branch protected
2. GitHub Actions CI: lint → test → build → deploy staging
3. README: Problem, Architecture (Mermaid), Stack, Quickstart, Demo (GIF/video)
4. Test coverage ≥80% (pytest + coverage)
5. Deployed ke staging (VPS/k8s/cloud) + monitoring