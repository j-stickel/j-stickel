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

**AI Systems Engineer.** I build production AI systems and run them: RAG pipelines, agentic assistants, fine-tuned models, and the infrastructure underneath.

The question behind all of it: how do you know an AI's numbers are true? My flagship system's retrieval recall is a measured 98%, up from 40% - but the number I'm proudest of is less flattering: the judge that grades every answer is itself audited, and that audit caught my system overfitting to my own tests by 7.7 points. The gap is published and recomputed on every run - and it widened from 6.3, which is exactly the early warning the number exists to give. Grade the grader; show the receipts.

---

### The work (case studies, in learning order)

<!-- This list mirrors mrjstickel-portfolio/src/data/projects.ts (the canonical case-study list + order) - sync it when that file changes. -->

One production system, built layer by layer. Every write-up below starts with something breaking - a chatbot lying, a judge grading its own homework, a VM freezing at 3am - and ends with a number proving it's fixed. It's all one codebase: Architecture Zero, four live white-label instances. Read them in order; they compound.

1. **[Hybrid RAG + Reranker](https://mrjstickel.com/projects/hybrid-rag)** - why a chatbot lies, and how retrieval gets fixed: vector search + a from-scratch BM25 + a local cross-encoder, recall 40% -> 93%, eval-driven.
2. **[RAG Ingestion Intelligence](https://mrjstickel.com/projects/rag-ingestion)** - when retrieval fails, fix the corpus: a stage-by-stage retrieval debugger, three measured rounds, 88% -> 100% recall with 44 of 50 hits at rank 1.
3. **[Context Engineering](https://mrjstickel.com/projects/context-engineering)** - keeping a RAG corpus honest: docs-as-code, single source of truth, and drift detection on both the write side and the read side. A stale source is a confident liar.
4. **[Grade the Grader](https://mrjstickel.com/projects/grade-the-grader)** - calibrating the LLM judge every other number depends on: planted errors, a human baseline, a second lab, an independently-authored second harness (RAGAS), and a locked holdout exam an outside model wrote - every instrument produced real findings, including a measured 6.3-point overfit gap published instead of hidden. The judge now carries a fourth rubric - refuse-vs-fabricate - measured at 12/12 over an artifact-demand cohort seeded from an external stress test.
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

### Now (updated 2026-07-26)

- **Grading the grader:** the LLM judge behind every trust number is now calibrated five independent ways - planted-error suite 31/31 across four rubrics, human-adjudicated agreement 90% (kappa 0.61), a second judge from a different lab at 99.0% correctness agreement (kappa 0.94, up from 92.7% / 0.68 before the judge was tightened - so an outside lab confirmed the tightening improved the instrument, not just its self-scores), and a second independently-authored harness (RAGAS) re-grading the same stored run with the same judge model: 98.2% agreement at the pass/fail boundary, its sole disagreement an already-known defect row. Every disagreement is hand-adjudicated - the latest six split into one real defect the primary judge had passed, one genuine corpus-staleness catch, and three refusal over-flags by the second judge.
- **The exam nobody could study for:** the fifth instrument is a locked holdout - 18 questions authored by an outside model straight from the corpus, structurally excluded from every fix loop. Latest run: tuned questions 91.0%, the holdout 83.3% - a 7.7-point overfit gap published as a first-class number, recomputed on every future run (it widened from 6.3 as tuning improved the home set while the stranger's exam held - exactly the warning the number exists to raise). Retrieval went 18 for 18 on the stranger's questions - twice now - pinning the whole gap to the answer layer.
- **Refuse-vs-fabricate, measured:** questions that demand artifacts the corpus does not hold (raw CSVs, shell commands, latency percentiles) run in every eval, scored by a fourth judge rubric - any invented path, command, or figure fails, even inside a disclosure-toned answer. Now a 13-question cohort holding 13/13, with the planted suite arbitrating: every planted fabrication mode caught on the first pass. The honesty behavior an external stress test praised, converted into a number that recomputes every run.
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
