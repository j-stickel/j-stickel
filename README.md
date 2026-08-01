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

The question behind all of it: how do you know an AI's numbers are true? My flagship system's retrieval recall measured 98% on the exam it was tuned against - and 91.6% on the harder, outside-authored exam that replaced it (2026-07-30). Both numbers are published, because the judge that grades every answer is itself audited, and that audit puts the overfit to my own tests at 11.3 points - a gap that has widened every time the exam got fairer, which is exactly the early warning it exists to give. Grade the grader; show the receipts.

---

### The work (case studies, in learning order)

<!-- This list mirrors mrjstickel-portfolio/src/data/projects.ts (the canonical case-study list + order) - sync it when that file changes. -->

One production system, built layer by layer. Every write-up below starts with something breaking - a chatbot lying, a judge grading its own homework, a VM freezing at 3am - and ends with a number proving it's fixed. It's all one codebase: Architecture Zero, four live white-label instances. Read them in order; they compound.

1. **[Hybrid RAG + Reranker](https://mrjstickel.com/projects/hybrid-rag)** - why a chatbot lies, and how retrieval gets fixed: vector search + a from-scratch BM25 + a local cross-encoder, recall 40% -> 93%, eval-driven.
2. **[RAG Ingestion Intelligence](https://mrjstickel.com/projects/rag-ingestion)** - when retrieval fails, fix the corpus: a stage-by-stage retrieval debugger, three measured rounds, 88% -> 100% recall with 44 of 50 hits at rank 1.
3. **[Context Engineering](https://mrjstickel.com/projects/context-engineering)** - keeping a RAG corpus honest: docs-as-code, single source of truth, and drift detection on both the write side and the read side. A stale source is a confident liar.
4. **[Grade the Grader](https://mrjstickel.com/projects/grade-the-grader)** - calibrating the LLM judge every other number depends on: planted errors, a human baseline, a second lab, an independently-authored second harness (RAGAS), and a locked holdout exam an outside model wrote - every instrument produced real findings, including a published overfit gap that widened from 6.3 to 11.3 points as the exam got fairer. The judge also carries a fourth rubric - refuse-vs-fabricate - holding 13/13 over an artifact-demand cohort seeded from an external stress test.
5. **[The External Stress Test](https://mrjstickel.com/projects/eval-stress-test)** - twelve adversarial demands for artifacts that do not exist, zero fabrications - and a demanded live eval run that caught a real regression, fixed and re-measured the same night.
6. **[Your Eval Score Is Measuring Three Things at Once](https://mrjstickel.com/projects/eval-score-three-things)** - a 5.9-point drop with zero code changes, decomposed instead of panicked over: a noise band, a retrieval diff that killed the obvious theory by direction, a silently rotted vector index, and a pre-registered prediction confirmed at 92.5% - with a corpus fingerprint on every eval row as the residue.
7. **[AI Security](https://mrjstickel.com/projects/ai-security)** - threat-modeling an AI that holds real data and can act: OWASP Web + LLM Top 10, a real broken-access-control bug found and fixed, CI security gates on every push.
8. **[Multi-Tier Access Isolation](https://mrjstickel.com/projects/multi-tier-isolation)** - proving a tiered AI cannot be talked into leaking: an adversarial cohort measured 3/11 -> 11/11 while owner recall held 100%. The corpus-diffusion lesson.
9. **[Zero-Trust Remote Inference](https://mrjstickel.com/projects/zero-trust-inference)** - a private GPU, reachable from anywhere, without opening a port: outbound-only tunnel, machine-to-machine service tokens, and a request served locally never egresses.
10. **[Ops Resilience](https://mrjstickel.com/projects/ops-resilience)** - backups that prove themselves every night: encrypted to two providers (one tamper-proof by object lock), pulled back and restore-drilled by machinery while I sleep.
11. **[The Night the VM Froze](https://mrjstickel.com/projects/incident-forensics)** - a batch job starved a production server for 17 minutes: the forensic chain, the OOM blind spot, and the layered guards that make it impossible again.
12. **[LLM Cost Engineering](https://mrjstickel.com/projects/llm-cost-engineering)** - prompt caching that proves itself in the token counters, and the double-billed system prompt the build found. Cost is a reliability metric.
13. **[Eco Mode](https://mrjstickel.com/projects/eco-mode)** - a federated RAG mesh: independent AI instances share knowledge at query time with fail-closed, per-caller scoped access. Never copied, never leaked.
14. **[Architecture Zero](https://mrjstickel.com/projects/az)** - the platform it all runs on: one core codebase, four live instances, white-label by config.

### The proof (live systems - click them)

- **[Northwind AI](https://northwind.mrjstickel.com)** - a live white-label demo of Architecture Zero. Ask it anything; flip the "View as" switcher and watch the access boundary work in real time.
- **[MrJStickel Assistant](https://ai.mrjstickel.com)** - my public AI, first person, RAG-loaded with my work history: the same assistant that lives in the corner of mrjstickel.com, standalone. Guest chat is open - interview it about my work. Its measured trust numbers are public at [ai.mrjstickel.com/#trust](https://ai.mrjstickel.com/#trust) - every value derived live from stored eval runs, shown as bands, never hand-set.
- **[JobTrue](https://jobtrue.ai)** - an AI job-search product, live with Stripe billing: honest 1-10 fit scoring, resume tailoring that structurally cannot fabricate (the model selects from your real bullets by index), cover letters, pipeline tracking. My own resume is served from it.
- **[thestatic.tv](https://thestatic.tv)** - a Web3 live-streaming platform built solo: 160+ API routes, GCP Livestream video, a real-time token economy, on-chain payments - the full-stack depth under the AI work.
- **[TheStatic.TV Agent](https://ai.thestatic.tv)** - that platform's public AI agent, on the same Architecture Zero core - open to guests, and reachable in-world inside the TheStatic HQ Decentraland scene. Its trust panel: [ai.thestatic.tv/#trust](https://ai.thestatic.tv/#trust).
- **[@thestatic-tv/dcl-sdk](https://www.npmjs.com/package/@thestatic-tv/dcl-sdk)** - a published TypeScript SDK for Decentraland scene integration.

### Now (updated 2026-08-01)

- **The trust layer went fleet-wide:** the four-rubric judged evals, honesty cohorts, and reranked hybrid retrieval now run on every serving instance - validated per instance with like-for-like A/Bs on each one's own question set (one peer: correctness +12; the other: right-document retrieval +18.4 with first-position hits doubled). Fixes are proven where they land, not assumed to transfer.
- **Live trust panels:** both public assistants now publish their measured numbers on public pages - every value derived from stored evaluation runs at request time, shown as bands across identical-configuration runs. The panel's first hour live caught a real measurement bug: bands were blending runs judged under two different rubric versions into one absurd spread. Fixed the same hour by stamping every eval row with a judge instrument version - a score is a property of the system, the corpus, the question set, AND the ruler.
- **Multi-turn, measure-gated:** scripted-conversation cohorts now measure follow-up handling - the failure class single-turn evals structurally cannot see. The discipline ran end to end: baselines on the real unresolved path (bare follow-ups found the right document 1 of 9 and 3 of 8 times on the two public instances), the follow-up resolver ported strictly on those numbers, and the same exams re-scored 8 of 9 and 7 of 8.
- **Grading the grader:** the LLM judge behind every trust number is now calibrated five independent ways - planted-error suite 32/32 across four rubrics, human-adjudicated agreement 90% (kappa 0.61), a second judge from a different lab at 99.0% correctness agreement (kappa 0.94, up from 92.7% / 0.68 before the judge was tightened - so an outside lab confirmed the tightening improved the instrument, not just its self-scores), and a second independently-authored harness (RAGAS) re-grading the same stored run with the same judge model: 98.2% agreement at the pass/fail boundary, its sole disagreement an already-known defect row. Every disagreement is hand-adjudicated - the latest six split into one real defect the primary judge had passed, one genuine corpus-staleness catch, and three refusal over-flags by the second judge.
- **The exam nobody could study for:** the fifth instrument is a locked holdout authored by an outside model straight from the corpus, structurally excluded from every fix loop - and the exam is held to the same standard as the system: the original 18 questions shared a lab with the judge, so a third lab re-authored it as 32 questions spanning the whole corpus, with the retired exam's authorship conflict priced first (2.1 points against a measured 1.5-point noise band). Latest run (2026-07-30): tuned questions 92.5%, the holdout 81.2% - an 11.3-point overfit gap published as a first-class number. The fairer exam also broke a flattering diagnosis: retrieval was 18-for-18 on the old exam but 25-of-32 on the new one - the old exam never reached the corpus tail, so "the gap lives entirely in the answer layer" was the exam talking, not the system. A fairer exam, a worse number, published anyway.
- **Refuse-vs-fabricate, measured everywhere:** questions that demand artifacts the corpus does not hold (raw CSVs, shell commands, secret values, private records) run on every serving instance, each cohort authored by a model that plays no other role in that instance's eval - the system never sets its own honesty exam. The private hub holds 13/13; both public assistants opened at 12/12 on their first measured reads; the public demo holds 100 across three consecutive runs. Any invented path, command, or figure fails, even inside a disclosure-toned answer.

---

### Tech

**AI / LLM** &nbsp;Python · FastAPI · RAG (ChromaDB, hybrid vector + BM25, cross-encoder reranking) · retrieval + answer-quality eval harnesses (LLM-as-judge: correctness, faithfulness, freshness) · judge calibration (planted-error suites, Cohen's kappa, cross-provider second opinions) · agentic tool use · QLoRA / PEFT fine-tuning · multi-provider routing (Anthropic, OpenAI, Gemini, Mistral, Groq, xAI, DeepSeek, Ollama) · local inference (7B to 30B-class on RTX 5090/3090)

**Full-stack** &nbsp;Next.js · React · TypeScript · React Native / Expo · Node.js · Firebase · Stripe

**Infrastructure** &nbsp;GCP · Docker · Nginx · Cloudflare · CI security gating (gitleaks, pip-audit, bandit, trivy)

---

### Open to

**AI / ML engineer roles** - building and operating production AI systems - and **private AI consulting** (your data, your brand, your infrastructure). &nbsp;[Resume](https://jobtrue.ai/u/mrjstickel/applied-ai-engineer) · [Get in touch](mailto:contact@mrjstickel.com)
