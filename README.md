<h2 align="left">Priyanka Bajaj</h2>

**Distinguished Engineer, AI & ML Systems · UBS London**

Building production AI agents, LLM evaluation frameworks, and MLOps infrastructure for Tier-1 financial institutions. Current focus: making AI systems that are explainable, auditable, and actually deployable in regulated environments — not just impressive in demos.

---

### What I work on

- **Multi-agent systems** — three-layer orchestration architecture: intent routing, specialist agents, reconciliation with human-in-the-loop escalation
- **LLM evaluation** — golden dataset frameworks, model-as-judge scoring, CI/CD regression gates aligned to FCA model risk standards
- **MLOps & CI/CD for ML** — Vertex AI pipelines, shadow deployments, automated rollback, full audit trails — cut model release cycles by 60%
- **RAG at scale** — hierarchical chunking, query rewriting, cross-encoder re-ranking, uncertainty thresholding for sub-second inference on millions of documents
- **Enterprise AI adoption** — bridging the gap between what AI can do in a lab and what Risk, Legal and Compliance will actually sign off on

---

### Open source repos

| Repo | Description |
|---|---|
| [llm-failure-taxonomy](https://github.com/priyanka25aug/llm-failure-taxonomy) | 6-class system-level LLM production failure taxonomy — 50 labeled incidents, rule-based + Claude API classifiers, failure budget calculator. Companion code for *Beyond Hallucination* (arXiv / MLSys 2026) |
| [enterprise-agent-framework](https://github.com/priyanka25aug/enterprise-agent-framework) | Production-grade multi-agent orchestration for regulated environments — router, specialist agents, reconciler, JSONL audit trail |
| [llm-evaluation-toolkit](https://github.com/priyanka25aug/llm-evaluation-toolkit) | Golden dataset evaluation harness, model-as-judge scoring, CI/CD regression gates for production LLM releases |
| [mlops-cicd-templates](https://github.com/priyanka25aug/mlops-cicd-templates) | GitHub Actions + Vertex AI ML pipelines — shadow deploys, canary rollouts, rollback scripts, BigQuery audit logging |
| [rag-production-patterns](https://github.com/priyanka25aug/rag-production-patterns) | Hierarchical chunking, query rewriting, re-ranking, uncertainty thresholding — RAG patterns that survive production |
| [financial-doc-intelligence](https://github.com/priyanka25aug/financial-doc-intelligence) | Document classification and extraction for financial documents with plain-English interpretability outputs |
| [gcp-vertex-ai-accelerators](https://github.com/priyanka25aug/gcp-vertex-ai-accelerators) | Vertex AI, BigQuery ML and Cloud Run utility scripts — reusable accelerators from real enterprise deployments |

---

### Publications

**[Beyond Hallucination: A System-Level Failure Taxonomy for Production LLMs](https://zenodo.org/records/15768800)** · Zenodo, 2026 · Sole author

Most LLM safety work focuses on hallucination. This paper argues that's the wrong frame — hallucination is one of six distinct failure classes, and roughly half of production failures are *silent* (no error signal, no flagged output). Introduces the FC-A/B/C/D failure budget framework with risk-tiered governance, a multi-label classifier (~88% accuracy), and a failure-budget calculator. Dataset: 50 annotated real-world production incidents.

---

### Upstream contributions

| Project | Contribution | Status |
|---|---|---|
| [Anthropic claude-cookbooks](https://github.com/anthropics/claude-cookbooks) | [08_The_compliance_aware_agent.ipynb](https://github.com/anthropics/claude-cookbooks/pull/783) — 44-cell notebook: FC-A/B/C/D failure budget framework, three-layer multi-agent orchestration, confidence-based escalation, human-in-the-loop for FCA/MiFID II/Basel III regulated environments | PR #783 · open |
| [Anthropic claude-cookbooks](https://github.com/anthropics/claude-cookbooks) | [evals/model_as_judge/](https://github.com/anthropics/claude-cookbooks/pull/786) — model-as-judge evaluation pipeline: golden dataset design, rubric scoring (0.99 judge-human correlation), regression gates, shadow deployment eval, CI entry point | PR #786 · open |
| [LangChain / LangGraph](https://github.com/langchain-ai/langgraph) | [compliance_checkpoint_fca_mifid2.ipynb](https://github.com/langchain-ai/langgraph/pull/8422) — compliance-aware HITL checkpoint: 4-node StateGraph, append-only SQLite audit trail (tamper-proof triggers), write-intent-before-execute pattern, uuid5 idempotency key, 5 runnable scenarios — FCA SYSC / MiFID II Art. 25 / SR 11-7 | PR #8422 · awaiting maintainer assignment |
| [NVIDIA NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails) | [financial_services_compliance_guardrails.ipynb](https://github.com/NVIDIA-NeMo/Guardrails/pull/2216) — GLiNER PII detection (IBAN, sort code, account number, NI number), MiFID II topic control via NIM, FCA COBS 4 disclaimer enforcement, Consumer Duty / SR 11-7 audit trail — 5 runnable scenarios with assertions | PR #2216 · open |
| [OpenHands](https://github.com/OpenHands/OpenHands) | [Financial document intelligence utility](https://github.com/OpenHands/OpenHands/pull/14271) — classifies earnings reports, loan agreements, audit reports and regulatory filings with plain-English risk outputs. No external APIs. | PR #14271 · under review |

---

### Stack

<!-- ML / AI -->
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![LlamaIndex](https://img.shields.io/badge/LlamaIndex-6B48FF?style=flat-square&logo=llamaindex&logoColor=white)

<!-- Eval / Ops -->
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

<!-- Infra / Cloud -->
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Vertex AI](https://img.shields.io/badge/Vertex_AI-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![BigQuery](https://img.shields.io/badge/BigQuery-4285F4?style=flat-square&logo=googlebigquery&logoColor=white)
![Cloud Run](https://img.shields.io/badge/Cloud_Run-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![AWS](https://img.shields.io/badge/AWS_SageMaker-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Azure](https://img.shields.io/badge/Azure_ML-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)

---

### Find me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/priyankabajaja/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/priyanka25aug)

---

### GitHub Stats

![GitHub Stats](https://github-readme-stats-sand-nine-94.vercel.app/api?username=priyanka25aug&show_icons=true&theme=default&hide_border=true&include_all_commits=true&rank_icon=github)
![Top Languages](https://github-readme-stats-sand-nine-94.vercel.app/api/top-langs/?username=priyanka25aug&layout=compact&hide_border=true&langs_count=6&hide=jupyter%20notebook,batchfile,shell&cache_seconds=1800)
