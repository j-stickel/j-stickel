### Hi, I'm Joseph Stickel (MrJStickel)

<p align="left">
  <a href="https://mrjstickel.com" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-mrjstickel.com-0891b2?style=for-the-badge" alt="Portfolio"/>
  </a>
  <a href="https://jobtrue.ai/u/mrjstickel/default-resume" target="_blank">
    <img src="https://img.shields.io/badge/Resume-jobtrue.ai-16a34a?style=for-the-badge" alt="Resume"/>
  </a>
  <a href="https://www.linkedin.com/in/mrjstickel" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-mrjstickel-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="mailto:contact@mrjstickel.com" target="_blank">
    <img src="https://img.shields.io/badge/Email-contact@mrjstickel.com-EA4335?style=for-the-badge" alt="Email"/>
  </a>
</p>

**AI Systems Engineer** - I design, ship, and operate production AI systems end to end: RAG pipelines, agentic assistants, fine-tuned models, and the platforms to run them. Solo, in production, measured. Retrieval recall on my flagship system: driven from 40% to a stamped 100% by a continuous eval harness.

---

### The work (case studies, in learning order)

Each write-up is a real production system with measured results - read them in order and they build on each other:

1. **[Hybrid RAG + Reranker](https://mrjstickel.com/projects/hybrid-rag)** - why a chatbot lies, and how retrieval gets fixed: vector search + a from-scratch BM25 + a local cross-encoder, recall 40% -> 93%, eval-driven.
2. **[RAG Ingestion Intelligence](https://mrjstickel.com/projects/rag-ingestion)** - when retrieval fails, fix the corpus: a stage-by-stage retrieval debugger, three measured rounds, 88% -> 100% recall with 44 of 50 hits at rank 1.
3. **[AI Security](https://mrjstickel.com/projects/ai-security)** - threat-modeling an AI that holds real data and can act: OWASP Web + LLM Top 10, a real broken-access-control bug found and fixed, CI security gates on every push.
4. **[Eco Mode](https://mrjstickel.com/projects/eco-mode)** - a federated RAG mesh: independent AI instances share knowledge at query time with fail-closed, per-caller scoped access. Never copied, never leaked.
5. **[Architecture Zero](https://mrjstickel.com/projects/az)** - the platform it all runs on: one core codebase, four live instances, white-label by config.

### The proof (live systems - click them)

- **[Northwind AI](https://northwind.mrjstickel.com)** - a live white-label demo of Architecture Zero. Ask it anything; flip the "View as" switcher and watch the access boundary work in real time.
- **[JobTrue](https://jobtrue.ai)** - an AI job-search product, live with Stripe billing: honest 1-10 fit scoring, resume tailoring that structurally cannot fabricate (the model selects from your real bullets by index), cover letters, pipeline tracking. My own resume is served from it.
- **[thestatic.tv](https://thestatic.tv)** - a Web3 live-streaming platform built solo: 160+ API routes, GCP Livestream video, a real-time token economy, on-chain payments - the full-stack depth under the AI work.
- **[@thestatic-tv/dcl-sdk](https://www.npmjs.com/package/@thestatic-tv/dcl-sdk)** - a published TypeScript SDK for Decentraland scene integration.

---

### Tech

**AI / LLM** &nbsp;Python · FastAPI · RAG (ChromaDB, hybrid vector + BM25, cross-encoder reranking) · retrieval eval harnesses · agentic tool use · QLoRA / PEFT fine-tuning · Claude / OpenAI / Ollama multi-provider routing · local inference (7B to 30B-class on RTX 5090/3090)

**Full-stack** &nbsp;Next.js · React · TypeScript · React Native / Expo · Node.js · Firebase · Stripe

**Infrastructure** &nbsp;GCP · Docker · Nginx · Cloudflare · CI security gating (gitleaks, pip-audit, bandit, trivy)

---

### Open to

**AI / ML engineer roles** - building and operating production AI systems - and **private AI consulting** (your data, your brand, your infrastructure). &nbsp;[Resume](https://jobtrue.ai/u/mrjstickel/default-resume) · [Get in touch](mailto:contact@mrjstickel.com)
