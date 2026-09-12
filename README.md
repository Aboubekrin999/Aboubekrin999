## Aboubekrin Mohamed Salem

Software engineer and MSc AI candidate based in Paris. I work in English and French.

Currently building at **[DAKAEI Technologies](https://dakaeitechnologies.com)** — client web, mobile, and AI work.

---

### What I'm building in the open

Three connected repositories around one problem: **reading academic papers is the bottleneck of an AI master's degree.** One user, one backend, three surfaces — a web app, a research model, and a mobile companion.

**[paper-companion](https://github.com/Aboubekrin999/paper-companion)** — RAG reading companion
`Next.js 16` · `FastAPI` · `Supabase pgvector` · `Claude`

Ingest pipeline (arXiv + PDF → parsed → chunked), a retrieval layer with a pluggable encoder protocol, a streaming chat orchestrator with prompt caching, and a retrieval eval harness with per-query metrics. **190 tests green, CI on every PR.** Magic-link auth and the library shell are implemented on the web side; the chat UI is not yet wired.

**[bilingual-section-classifier](https://github.com/Aboubekrin999/bilingual-section-classifier)** — XLM-RoBERTa fine-tune, EN + FR
`PyTorch` · `Hugging Face` · `Weights & Biases`

Classifies paper passages by section type, so retrieval can tell *"what did they actually do"* from *"what is the prior art."* French scientific writing — HAL, INRIA, university theses — is underserved by English-only classifiers. Label schema, dataset pipeline, language-stratified splits, training and eval scripts are in. **94 tests green.** The training run itself hasn't been executed yet.

**[paper-flashcards](https://github.com/Aboubekrin999/paper-flashcards)** — mobile companion
`React Native` · `Expo` · `TypeScript`

Spaced-repetition cards generated from papers already in your library, built on paper-companion's backend rather than a second ingest pipeline. Scaffold and CI are in place; the feature build hasn't started.

*These paused in May 2026 while client delivery took priority. Each README states plainly what is built and what is still planned — no roadmap item is described as shipped.*

---

### How I go from problem to product

Each of these repos has a `docs/DECISIONS.md` and a `docs/ROADMAP.md` that were written **before** the code. I do the product work — problem, user, scope, tradeoffs — as a written artifact, then build against it.

**Problem, user, and scope before implementation.** Every README opens with the problem, who it's for, and an explicit *out of scope* list — deciding what not to build is most of the work. → [scope example](https://github.com/Aboubekrin999/paper-companion#what-v1-does)

**Product and technical decisions recorded with their rationale.** Numbered ADRs covering each tradeoff, what the choice costs, and what would trigger reversing it. → [ADRs](https://github.com/Aboubekrin999/paper-companion/blob/main/docs/DECISIONS.md)

**Evaluation designed to expose failure, not flatter it.** The classifier reports F1 per language on a language-stratified test set, because a single macro number hides asymmetric performance between EN and FR. → [eval design](https://github.com/Aboubekrin999/bilingual-section-classifier/blob/main/docs/DECISIONS.md)

**Milestones that end in something demonstrable.** Roadmaps are week-by-week, each week closing on a working checkpoint a user could try rather than a percentage complete. → [roadmap](https://github.com/Aboubekrin999/paper-companion/blob/main/docs/ROADMAP.md)

---

### Stack

**Languages** Python · TypeScript · PHP · Java · C/C++
**Backend** FastAPI · Laravel · Node.js · Django
**Frontend** Next.js · React · Tailwind
**Mobile** React Native / Expo · Flutter
**ML** PyTorch · Hugging Face Transformers · pgvector · Claude API
**Data & infra** PostgreSQL / Supabase · Docker · Vercel · GitHub Actions

---

📍 Paris, France  ·  ✉️ [aboubekrinmouhamedsalem@gmail.com](mailto:aboubekrinmouhamedsalem@gmail.com)
