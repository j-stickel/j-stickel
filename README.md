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

**AI Systems Engineer** - I design, ship, and operate production AI systems end to end: RAG pipelines, agentic assistants, fine-tuned models, and the platforms to run them. Solo, in production, measured. Retrieval recall on my flagship system: driven from 40% to a stamped 100% by a continuous eval harness - which now also judges every answer for faithfulness to its sources (100% on the latest full run).

---

### The work (case studies, in learning order)

<!-- This list mirrors mrjstickel-portfolio/src/data/projects.ts (the canonical case-study list + order) - sync it when that file changes. -->

Each write-up is a real production system with measured results - read them in order and they build on each other:

1. **[Hybrid RAG + Reranker](https://mrjstickel.com/projects/hybrid-rag)** - why a chatbot lies, and how retrieval gets fixed: vector search + a from-scratch BM25 + a local cross-encoder, recall 40% -> 93%, eval-driven.
2. **[RAG Ingestion Intelligence](https://mrjstickel.com/projects/rag-ingestion)** - when retrieval fails, fix the corpus: a stage-by-stage retrieval debugger, three measured rounds, 88% -> 100% recall with 44 of 50 hits at rank 1.
3. **[Context Engineering](https://mrjstickel.com/projects/context-engineering)** - keeping a RAG corpus honest: docs-as-code, single source of truth, and drift detection on both the write side and the read side. A stale source is a confident liar.
4. **[AI Security](https://mrjstickel.com/projects/ai-security)** - threat-modeling an AI that holds real data and can act: OWASP Web + LLM Top 10, a real broken-access-control bug found and fixed, CI security gates on every push.
5. **[Zero-Trust Remote Inference](https://mrjstickel.com/projects/zero-trust-inference)** - a private GPU, reachable from anywhere, without opening a port: outbound-only tunnel, machine-to-machine service tokens, and a request served locally never egresses.
6. **[Ops Resilience](https://mrjstickel.com/projects/ops-resilience)** - backups that prove themselves every night: encrypted to two providers (one tamper-proof by object lock), pulled back and restore-drilled by machinery while I sleep.
7. **[The Night the VM Froze](https://mrjstickel.com/projects/incident-forensics)** - a batch job starved a production server for 17 minutes: the forensic chain, the OOM blind spot, and the layered guards that make it impossible again.
8. **[Eco Mode](https://mrjstickel.com/projects/eco-mode)** - a federated RAG mesh: independent AI instances share knowledge at query time with fail-closed, per-caller scoped access. Never copied, never leaked.
9. **[Architecture Zero](https://mrjstickel.com/projects/az)** - the platform it all runs on: one core codebase, four live instances, white-label by config.

### The proof (live systems - click them)

- **[Northwind AI](https://northwind.mrjstickel.com)** - a live white-label demo of Architecture Zero. Ask it anything; flip the "View as" switcher and watch the access boundary work in real time.
- **[MrJStickel Assistant](https://ai.mrjstickel.com)** - my public AI, first person, RAG-loaded with my work history: the same assistant that lives in the corner of mrjstickel.com, standalone. Guest chat is open - interview it about my work.
- **[JobTrue](https://jobtrue.ai)** - an AI job-search product, live with Stripe billing: honest 1-10 fit scoring, resume tailoring that structurally cannot fabricate (the model selects from your real bullets by index), cover letters, pipeline tracking. My own resume is served from it.
- **[thestatic.tv](https://thestatic.tv)** - a Web3 live-streaming platform built solo: 160+ API routes, GCP Livestream video, a real-time token economy, on-chain payments - the full-stack depth under the AI work.
- **[TheStatic.TV Agent](https://ai.thestatic.tv)** - that platform's public AI agent, on the same Architecture Zero core - open to guests, and reachable in-world inside the TheStatic HQ Decentraland scene.
- **[@thestatic-tv/dcl-sdk](https://www.npmjs.com/package/@thestatic-tv/dcl-sdk)** - a published TypeScript SDK for Decentraland scene integration.

### Now (updated 2026-07-16)

- **Answer-trust layer:** every eval answer is LLM-judged for correctness AND faithfulness to the context it actually saw - latest full run: 98% recall, 85.5% correct, 100% faithful. Correct and grounded are different failures; I measure both.
- **The complete trust map:** a live panel tracking 41 industry trust/eval capabilities (guardrails, injection gates, judge reliability, freshness) with honest statuses - measured, built, or not yet. No number renders unless it derives from a live source.
- **Boring on purpose:** nightly encrypted backups to two destinations, plus a nightly restore drill that rehearses recovery by machinery. An untested backup is a hope.

---

### Tech

**AI / LLM** &nbsp;Python · FastAPI · RAG (ChromaDB, hybrid vector + BM25, cross-encoder reranking) · retrieval + answer-quality eval harnesses (LLM-as-judge: correctness, faithfulness) · agentic tool use · QLoRA / PEFT fine-tuning · Claude / OpenAI / Ollama multi-provider routing · local inference (7B to 30B-class on RTX 5090/3090)

**Full-stack** &nbsp;Next.js · React · TypeScript · React Native / Expo · Node.js · Firebase · Stripe

**Infrastructure** &nbsp;GCP · Docker · Nginx · Cloudflare · CI security gating (gitleaks, pip-audit, bandit, trivy)

---

### Open to

**AI / ML engineer roles** - building and operating production AI systems - and **private AI consulting** (your data, your brand, your infrastructure). &nbsp;[Resume](https://jobtrue.ai/u/mrjstickel/applied-ai-engineer) · [Get in touch](mailto:contact@mrjstickel.com)
