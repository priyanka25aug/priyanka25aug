<h2 align="left">Priyanka Bajaj</h2>

**Distinguished Engineer, AI & ML Systems · UBS London**

Building production AI agents, LLM inference infrastructure, evaluation frameworks, and MLOps for Tier-1 financial institutions. Current focus: making AI systems that are explainable, auditable, and actually deployable in regulated environments — not just impressive in demos.

---

### What I work on

- **LLM inference & GPU serving** — vLLM, TensorRT-LLM, speculative decoding (γ-sweep acceptance-rate analysis), KV-cache/prefix-caching characterisation, dynamic per-token FP8 quantization, fused CUDA kernels
- **Multi-agent systems** — three-layer orchestration architecture: intent routing, specialist agents, reconciliation with human-in-the-loop escalation
- **LLM evaluation** — golden dataset frameworks, model-as-judge scoring, CI/CD regression gates aligned to FCA model risk standards
- **LLM training pipelines** — pretraining data quality (MinHash+LSH dedup, perplexity filtering), curriculum design, training-stability monitoring
- **MLOps & CI/CD for ML** — Vertex AI pipelines, shadow deployments, automated rollback, full audit trails — cut model release cycles by 60%
- **RAG at scale** — hierarchical chunking, query rewriting, cross-encoder re-ranking, uncertainty thresholding for sub-second inference on millions of documents
- **Enterprise AI adoption** — bridging the gap between what AI can do in a lab and what Risk, Legal and Compliance will actually sign off on

---

### Open source repos

| Repo | Description |
|---|---|
| [llm-failure-taxonomy](https://github.com/priyanka25aug/llm-failure-taxonomy) | 6-class system-level LLM production failure taxonomy — 50 labeled incidents, rule-based + Claude API classifiers, failure budget calculator. Companion code for *Evaluation Blindness* (arXiv 2026) |
| [gpu-llm-profiler](https://github.com/priyanka25aug/gpu-llm-profiler) | NVIDIA GPU inference profiler — speculative decoding acceptance-rate sweep (γ 1–8), KV cache hit rate vs context length (with/without prefix caching), AWQ / GPTQ / FP16 throughput comparison. Built on vLLM. 14 unit tests run GPU-free. |
| [llm-pretraining-toolkit](https://github.com/priyanka25aug/llm-pretraining-toolkit) | Pretraining data quality, curriculum design and training stability — from-scratch MinHash+LSH near-duplicate detection, perplexity filtering (KenLM/GPT-2 backends), fastText language gating, difficulty-scored curriculum mixing with decay schedules, rolling z-score loss-spike detection with rollback flags, per-layer gradient-norm tracking, HF-compatible dataset cards. 34 tests, NumPy-only core, Apache-2.0. |
| [enterprise-agent-framework](https://github.com/priyanka25aug/enterprise-agent-framework) | Production-grade multi-agent orchestration for regulated environments — router, specialist agents, reconciler, JSONL audit trail |
| [llm-evaluation-toolkit](https://github.com/priyanka25aug/llm-evaluation-toolkit) | Golden dataset evaluation harness, model-as-judge scoring, CI/CD regression gates for production LLM releases |
| [mlops-cicd-templates](https://github.com/priyanka25aug/mlops-cicd-templates) | GitHub Actions + Vertex AI ML pipelines — shadow deploys, canary rollouts, rollback scripts, BigQuery audit logging |
| [rag-production-patterns](https://github.com/priyanka25aug/rag-production-patterns) | Hierarchical chunking, query rewriting, re-ranking, uncertainty thresholding — RAG patterns that survive production |
| [financial-doc-intelligence](https://github.com/priyanka25aug/financial-doc-intelligence) | Document classification and extraction for financial documents with plain-English interpretability outputs |
| [gcp-vertex-ai-accelerators](https://github.com/priyanka25aug/gcp-vertex-ai-accelerators) | Vertex AI, BigQuery ML and Cloud Run utility scripts — reusable accelerators from real enterprise deployments |

---

### Publications

**[Evaluation Blindness: How Silent Measurement Failures Corrupt AI Systems from Training to Deployment](https://arxiv.org/abs/2608.02786)** · arXiv:2608.02786, August 2026 · Independent research · Sole author

Most measurement failures in AI systems produce no error signal — the failure propagates silently through training loops, evaluation pipelines, and production monitoring until downstream harm makes it visible. This paper formalises *evaluation blindness* as the unifying property of this failure mode and shows it operates at two stages the literature has treated separately: training time (reward hacking, importance-sampling bugs, benchmark contamination) and deployment time (six production failure classes, 53% silent across 50 real-world incidents). Introduces a detectability predicate unifying both stages, four concrete training-time case studies including a TRL PR #6594 implementation bug, and a per-use-case failure budget framework tied to risk class. Code and taxonomy: [github.com/priyanka25aug/llm-failure-taxonomy](https://github.com/priyanka25aug/llm-failure-taxonomy)

**[Beyond Hallucination: A System-Level Failure Taxonomy for Production LLMs](https://zenodo.org/records/15768800)** · Zenodo, 2026 · Sole author

Earlier version of the taxonomy work. Introduces the FC-A/B/C/D failure budget framework with risk-tiered governance, a multi-label classifier (~88% accuracy), and a failure-budget calculator built on 50 annotated real-world production incidents.

---

### Upstream contributions

| Project | Contribution | Status |
|---|---|---|
| [TransformerLens](https://github.com/TransformerLensOrg/TransformerLens) | [PR #1574 — Jacobian Lens fit-checkpoint loader](https://github.com/TransformerLensOrg/TransformerLens/pull/1574) — `JacobianLens.load()` now accepts `anthropics/jacobian-lens` fit-checkpoints (6-key reference format: `jacobian_sum`, `n_done`, `next_idx`, `target_layer`, `skip_first`, `source_layers`), infers `d_model` from matrix shape, harvests top-level `target_layer` for `validate_model()`, converts to standard TL artifact. Three rounds of maintainer review. | PR #1574 · **merged** |
| [TransformerLens](https://github.com/TransformerLensOrg/TransformerLens) | [PR #1600 — Migration guide: boot_native train-from-scratch recipe](https://github.com/TransformerLensOrg/TransformerLens/pull/1600) — added `boot_native` recipe to `migrating_to_v3.md` covering custom training loops with the new bridge API. | PR #1600 · **merged** |
| [HuggingFace TRL](https://github.com/huggingface/trl) | [PR #6621 — Activation offloading for GRPOTrainer and RLOOTrainer](https://github.com/huggingface/trl/pull/6621) — opt-in `activation_offloading` flag mirroring the DPO/KTO pattern; `GRPOConfig` and `RLOOConfig` extended; slow tests parametrized over Llama 3.2 and Mistral 0.2. Completes issue #3717. | PR #6621 · open |
| [docker/docker-agent](https://github.com/docker/docker-agent) | [PR #3857 — GITHUB_TOKEN forwarding for eval containers](https://github.com/docker/docker-agent/pull/3857) — documents GITHUB_TOKEN forwarding pattern for Docker eval containers. | PR #3857 · **merged** |
| [Anthropic claude-cookbooks](https://github.com/anthropics/claude-cookbooks) | [08_The_compliance_aware_agent.ipynb](https://github.com/anthropics/claude-cookbooks/pull/783) — 44-cell notebook: FC-A/B/C/D failure budget framework, three-layer multi-agent orchestration, confidence-based escalation, human-in-the-loop for FCA/MiFID II/Basel III regulated environments | PR #783 · open |
| [Anthropic claude-cookbooks](https://github.com/anthropics/claude-cookbooks) | [evals/model_as_judge/](https://github.com/anthropics/claude-cookbooks/pull/786) — model-as-judge evaluation pipeline: golden dataset design, rubric scoring (0.99 judge-human correlation), regression gates, shadow deployment eval, CI entry point | PR #786 · open |
| [LangChain / LangGraph](https://github.com/langchain-ai/langgraph) | [compliance_checkpoint_fca_mifid2.ipynb](https://github.com/langchain-ai/langgraph/pull/8422) — compliance-aware HITL checkpoint: 4-node StateGraph, append-only SQLite audit trail (tamper-proof triggers), write-intent-before-execute pattern, uuid5 idempotency key, 5 runnable scenarios — FCA SYSC / MiFID II Art. 25 / SR 11-7 | PR #8422 · awaiting maintainer assignment |
| [NVIDIA NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails) | [financial_services_compliance_guardrails.ipynb](https://github.com/NVIDIA-NeMo/Guardrails/pull/2216) — GLiNER PII detection (IBAN, sort code, account number, NI number), MiFID II topic control via NIM, FCA COBS 4 disclaimer enforcement, Consumer Duty / SR 11-7 audit trail — 5 runnable scenarios with assertions | PR #2216 · open |
| [HuggingFace evaluate](https://github.com/huggingface/evaluate) | [financial_llm_faithfulness](https://github.com/huggingface/evaluate/pull/783) — rule-based metric for regulated financial AI: numerical faithfulness (% / bps / monetary values vs reference), FCA COBS 4 / MiFID II disclaimer detection, composite compliance risk score (0–1). First financial metric in the library. Deterministic — no external APIs. | PR #783 · open |
| [OpenHands](https://github.com/OpenHands/OpenHands) | [Financial document intelligence utility](https://github.com/OpenHands/OpenHands/pull/14271) — classifies earnings reports, loan agreements, audit reports and regulatory filings with plain-English risk outputs. No external APIs. | PR #14271 · under review |
| [vLLM](https://github.com/vllm-project/vllm) | [benchmarks/benchmark_spec_decode_analysis.py](https://github.com/vllm-project/vllm/pull/49825) — speculative decoding analysis script: sweeps gamma (1–8), records acceptance rate (α = (speedup−1)/γ), tok/s, p50/p95/p99 latency, GPU memory. First spec decode analysis script in vllm/benchmarks/. SSH-signed. | PR #49825 · open |
| [vLLM](https://github.com/vllm-project/vllm) | [silu_and_mul_dynamic_per_token_quant CUDA kernel](https://github.com/vllm-project/vllm/pull/49828) — fused SiLU+gating + dynamic per-token FP8 quantization kernel. Two-phase: Phase 1 computes per-token absmax via warp_max + shared memory reduction; Phase 2 quantizes to FP8. Fills gap left by existing per-tensor silu_and_mul_quant. Addresses Q3 2026 SIG-Quantization roadmap item #48168. | PR #49828 · open |
| [flash-attention](https://github.com/Dao-AILab/flash-attention) | [tests/test_flash_attn_gqa_decode.py](https://github.com/Dao-AILab/flash-attention/pull/2730) — 6 test groups for production LLM serving gaps: GQA extreme ratios (8:1/16:1/32:1 — Llama 3 70B patterns), speculative decode verify phase (seqlen_q=2–8), chunked prefill+decode varlen mixed batches, paged KV small block sizes [16,32,128], softcap+GQA decode, long context (8k/16k) GQA backward. SSH-signed. | PR #2730 · open |

---

### Stack

<!-- ML / AI -->
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)
![vLLM](https://img.shields.io/badge/vLLM-1E90FF?style=flat-square)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
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
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)
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
