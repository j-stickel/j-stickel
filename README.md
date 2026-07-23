### Hi, I'm Joseph Stickel (MrJStickel)

<p align="left">
  <a href="https://mrjstickel.com" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-mrjstickel.com-0891b2?style=for-the-badge" alt="Portfolio"/>
  </a>
  <a href="https://jobtrue.ai/u/mrjstickel/applied-ai-engineer" target="_blank">
    <img src="https://img.shields.io/badge/Resume-jobtrue.ai-16a34a?style=for-the-badge" alt="Resume"/>
  </a>
  <a href="https://www.linkedin.com/in/mrjstickel" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-mrjstickel-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="mailto:contact@mrjstickel.com" target="_blank">
    <img src="https://img.shields.io/badge/Email-contact@mrjstickel.com-EA4335?style=for-the-badge" alt="Email"/>
  </a>
</p>

**AI Systems Engineer** - I design, ship, and operate production AI systems end to end: RAG pipelines, agentic assistants, fine-tuned models, and the platforms to run them. Solo, in production, measured. Retrieval recall on my flagship system: driven from 40% to a measured 98% floor on a frozen regression set - and the LLM judge that grades every answer is itself calibrated three ways (planted errors 15/15, human-adjudicated kappa 0.61, second-lab agreement 92.7%). I do not just publish numbers; I grade the grader behind them.

---

### The work (case studies, in learning order)

<!-- This list mirrors mrjstickel-portfolio/src/data/projects.ts (the canonical case-study list + order) - sync it when that file changes. -->

Each write-up is a real production system with measured results - read them in order and they build on each other:

1. **[Hybrid RAG + Reranker](https://mrjstickel.com/projects/hybrid-rag)** - why a chatbot lies, and how retrieval gets fixed: vector search + a from-scratch BM25 + a local cross-encoder, recall 40% -> 93%, eval-driven.
2. **[RAG Ingestion Intelligence](https://mrjstickel.com/projects/rag-ingestion)** - when retrieval fails, fix the corpus: a stage-by-stage retrieval debugger, three measured rounds, 88% -> 100% recall with 44 of 50 hits at rank 1.
3. **[Context Engineering](https://mrjstickel.com/projects/context-engineering)** - keeping a RAG corpus honest: docs-as-code, single source of truth, and drift detection on both the write side and the read side. A stale source is a confident liar.
4. **[Grade the Grader](https://mrjstickel.com/projects/grade-the-grader)** - calibrating the LLM judge every other number depends on: planted errors, a human baseline, a second lab - all three found real instrument defects, fixed and re-measured.
5. **[The External Stress Test](https://mrjstickel.com/projects/eval-stress-test)** - twelve adversarial demands for artifacts that do not exist, zero fabrications - and a demanded live eval run that caught a real regression, fixed and re-measured the same night.
6. **[AI Security](https://mrjstickel.com/projects/ai-security)** - threat-modeling an AI that holds real data and can act: OWASP Web + LLM Top 10, a real broken-access-control bug found and fixed, CI security gates on every push.
7. **[Multi-Tier Access Isolation](https://mrjstickel.com/projects/multi-tier-isolation)** - proving a tiered AI cannot be talked into leaking: an adversarial cohort measured 3/11 -> 11/11 while owner recall held 100%. The corpus-diffusion lesson.
8. **[Zero-Trust Remote Inference](https://mrjstickel.com/projects/zero-trust-inference)** - a private GPU, reachable from anywhere, without opening a port: outbound-only tunnel, machine-to-machine service tokens, and a request served locally never egresses.
9. **[Ops Resilience](https://mrjstickel.com/projects/ops-resilience)** - backups that prove themselves every night: encrypted to two providers (one tamper-proof by object lock), pulled back and restore-drilled by machinery while I sleep.
10. **[The Night the VM Froze](https://mrjstickel.com/projects/incident-forensics)** - a batch job starved a production server for 17 minutes: the forensic chain, the OOM blind spot, and the layered guards that make it impossible again.
11. **[LLM Cost Engineering](https://mrjstickel.com/projects/llm-cost-engineering)** - prompt caching that proves itself in the token counters, and the double-billed system prompt the build found. Cost is a reliability metric.
12. **[Eco Mode](https://mrjstickel.com/projects/eco-mode)** - a federated RAG mesh: independent AI instances share knowledge at query time with fail-closed, per-caller scoped access. Never copied, never leaked.
13. **[Architecture Zero](https://mrjstickel.com/projects/az)** - the platform it all runs on: one core codebase, four live instances, white-label by config.

### The proof (live systems - click them)

- **[Northwind AI](https://northwind.mrjstickel.com)** - a live white-label demo of Architecture Zero. Ask it anything; flip the "View as" switcher and watch the access boundary work in real time.
- **[MrJStickel Assistant](https://ai.mrjstickel.com)** - my public AI, first person, RAG-loaded with my work history: the same assistant that lives in the corner of mrjstickel.com, standalone. Guest chat is open - interview it about my work.
- **[JobTrue](https://jobtrue.ai)** - an AI job-search product, live with Stripe billing: honest 1-10 fit scoring, resume tailoring that structurally cannot fabricate (the model selects from your real bullets by index), cover letters, pipeline tracking. My own resume is served from it.
- **[thestatic.tv](https://thestatic.tv)** - a Web3 live-streaming platform built solo: 160+ API routes, GCP Livestream video, a real-time token economy, on-chain payments - the full-stack depth under the AI work.
- **[TheStatic.TV Agent](https://ai.thestatic.tv)** - that platform's public AI agent, on the same Architecture Zero core - open to guests, and reachable in-world inside the TheStatic HQ Decentraland scene.
- **[@thestatic-tv/dcl-sdk](https://www.npmjs.com/package/@thestatic-tv/dcl-sdk)** - a published TypeScript SDK for Decentraland scene integration.

### Now (updated 2026-07-23)

- **Grading the grader:** the LLM judge behind every trust number is now calibrated three independent ways - planted-error suite 15/15, human-adjudicated agreement 90% (kappa 0.61), and a second judge from a different lab at 92.7% agreement with all 8 disagreements hand-adjudicated. All three found real instrument defects; all are fixed and regression-tested. Next: a second independently-authored harness and a locked holdout set.
- **Isolation you can measure:** multi-tier access isolation driven 3/11 -> 11/11 on an adversarial cohort (injection, confabulation bait, social engineering) while owner recall held at 100% - the write-up covers why classifying one folder barely moved the number.
- **Six providers, one adapter:** a multi-provider registry (Anthropic, OpenAI, Gemini, Mistral, Groq, xAI, DeepSeek, plus local Ollama) where adding a provider is config, not code - built to pin a cross-provider judge, kept because customers pick their own model.

---

### Tech

**AI / LLM** &nbsp;Python · FastAPI · RAG (ChromaDB, hybrid vector + BM25, cross-encoder reranking) · retrieval + answer-quality eval harnesses (LLM-as-judge: correctness, faithfulness, freshness) · judge calibration (planted-error suites, Cohen's kappa, cross-provider second opinions) · agentic tool use · QLoRA / PEFT fine-tuning · multi-provider routing (Anthropic, OpenAI, Gemini, Mistral, Groq, xAI, DeepSeek, Ollama) · local inference (7B to 30B-class on RTX 5090/3090)

**Full-stack** &nbsp;Next.js · React · TypeScript · React Native / Expo · Node.js · Firebase · Stripe

**Infrastructure** &nbsp;GCP · Docker · Nginx · Cloudflare · CI security gating (gitleaks, pip-audit, bandit, trivy)

---

### Open to

**AI / ML engineer roles** - building and operating production AI systems - and **private AI consulting** (your data, your brand, your infrastructure). &nbsp;[Resume](https://jobtrue.ai/u/mrjstickel/applied-ai-engineer) · [Get in touch](mailto:contact@mrjstickel.com)
