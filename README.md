<img src="./banner.svg" alt="Vikas Srinivasa · Applied AI Engineer · Building AI that knows when it can be trusted" width="100%"/> <p> <a href="https://www.linkedin.com/in/vikas-srinivasa"><img src="https://img.shields.io/badge/LinkedIn-171a1d?style=for-the-badge&logo=linkedin&logoColor=white"/></a> <a href="https://hashnode.com/@vikassrinivasa"><img src="https://img.shields.io/badge/Blog-332827?style=for-the-badge&logo=hashnode&logoColor=white"/></a> <a href="https://medium.com/@vikassrinivasa"><img src="https://img.shields.io/badge/Medium-814738?style=for-the-badge&logo=medium&logoColor=white"/></a> <a href="https://vikassrini.github.io/"><img src="https://img.shields.io/badge/Portfolio-d97b4a?style=for-the-badge&logo=githubpages&logoColor=white"/></a> <a href="mailto:srinivasavikas0@gmail.com"><img src="https://img.shields.io/badge/Email-f5c583?style=for-the-badge&logo=gmail&logoColor=white"/></a> </p>

My path into AI started on a cricket field. I played cricket professionally until a back injury ended that career. Seven years after my initial studies, I went back to complete my degree in Computer Science, and that's where I found AI.

Today I'm an Applied AI Engineer who builds AI systems that know when they can be trusted. I have built conversational RAG over dense policy documents, worked hands-on with LLM fine-tuning, and turned loosely specified problems into working ML and NLP systems across health, finance, industrial and security domains.
My strongest work is the evaluation that decides where a model can act on its own and where a person must step in. Most recently, I built a human-in-the-loop classifier that automates 51% of decisions at 99.18% accuracy, and grew a library of ~40 broken security detections into 421+ graph-based rules.

I also love writing about tech, especially explaining the intuition behind complex topics so they click for anyone, not just specialists. My blog series on transformers and LLM fine-tuning are a good place to start.

---

## 📋 Career Scorecard

| Innings | Team | Role | Player of the match moment |
|:--|:--|:--|:--|
| 2026 – not out | **Orange Ladders** | AI Consultant | 🎯 Automated **51.1%** of decisions at **99.18%** accuracy. The other 48.9% go to humans, on purpose. |
| 2026 – not out | **Stealth cybersecurity startup** | Founding Engineer | 🛡️ Inherited ~40 broken detections. Left with **421+** working ones. |
| 2025 – 26 | **GrowthArc** | AI Engineer | 🔧 Predicted device failures **7 days early** at ~0.90 PR-AUC |
| 2024 – not out | **IntuitiFi** | Co-Founder | 💬 Built an assistant that reads insurance policies so you don't have to |
| 2023 | **Toosi** | AI Intern | 🎓 Fine-tuned Llama 2. Learned the hard way when *not* to. |

---

## 🧭 My Entire Philosophy, in One Flowchart

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#26233a','primaryTextColor':'#e0def4','primaryBorderColor':'#c4a7e7','lineColor':'#ebbcba','secondaryColor':'#1f1d2e','tertiaryColor':'#191724','fontFamily':'Segoe UI, Helvetica, Arial, sans-serif'}}}%%
flowchart LR
    A[Model makes a prediction] --> B{Confident enough?<br/><i>and can it prove it?</i>}
    B -- Yes --> C[✅ Ship it]
    B -- No --> D[🙋 Ask a human]
    D -. lessons learned .-> A
```

**Three rules I'd tattoo on a model if I could:**

1. **"95% accurate" is a vibe, not a guarantee.** I want to know *where* the model is right, not just how often.
2. **Unseen data is the real exam.** My predictive-maintenance model scored ~0.90 on devices it knew and ~0.41 on ones it didn't. I report both. The second number is the honest one.
3. **"We added an LLM" is not a result.** Ablate, or it didn't happen.

---

## 🔬 Tales from the Trenches

<details>
<summary><b>I fine-tuned Llama 2. It forgot everything else.</b></summary>

<br/>

At Toosi I crawled travel data with **Scrapy**, cleaned it into a training set, and fine-tuned **Llama 2 with LoRA** on RunPod GPUs. It became a travel expert and promptly forgot how to be anything else (hello, **catastrophic forgetting**). So I switched to **RAG**, keeping the knowledge in retrieval instead of cramming it into the weights.

**Lesson:** fine-tuning teaches a model *how* to talk; retrieval tells it *what's true*. Know which one you need.

</details>

<details>
<summary><b>The LLM wrote hundreds of security rules. They looked perfect. None of them worked.</b></summary>

<br/>

The LLM-generated detections were confident, well formatted and completely disconnected from the real graph schema, so they never fired. I fixed this by giving the generator explicit **entity and relationship contracts**, then testing every rule with positive, negative and near-miss cases. Result: **~40 → 421+** working graph detections on **Neo4j**.

**Lesson:** plausible ≠ valid. LLMs are great at sounding right.

</details>

<details>
<summary><b>Reading insurance policies so you don't have to</b></summary>

<br/>

Health-insurance policies are long, dense and somehow designed so nobody reads them. This assistant lets people just ask. **Unstructured.io** extracts the documents, **Weaviate** retrieves the right clauses, **GPT-4 Turbo** answers from them, and **FastAPI + WebSockets** keep the conversation going even when connections don't.

</details>

<details>
<summary><b>🔧 Predicting failures a week early (0.08% of the data, 100% of the drama)</b></summary>

<br/>

Same-day failure detection is just bad news delivered on time, so I reframed it as a **7-day early warning**: ~125K daily records, 803 devices, a ~0.08% failure rate and 262 engineered features. With imbalance like that, a model that always says "fine" is 99.9% accurate and 100% useless, so everything was judged on **PR-AUC**.

</details>

<details>
<summary><b>📐 Teaching a fuel tank to change size without losing its shape</b></summary>

<br/>

I parsed STEP assemblies into **point clouds** and geometry metadata (OpenCascade) for shape-based search. Then I automated a fuel-tank redesign in **FreeCAD + Python**: new volume targets, fixed dimensions held, and inlet/outlet holes moved so everything still fits.

</details>

---

## ✍️ I Explain the Intuition

Because "it's just matrix multiplication" has never helped anyone understand anything.

<a href="https://blog.vikassrinivasa.dev/series/transformer-intuition-explained"><img src="https://img.shields.io/badge/Series-Transformers:_Intuition_%26_Beyond-191724?style=for-the-badge&logo=hashnode&logoColor=white"/></a>
<a href="https://intuitive-fine-tuning.hashnode.dev/"><img src="https://img.shields.io/badge/Series-The_Intuitive_Fine--Tuning_Series-eb6f92?style=for-the-badge&logo=hashnode&logoColor=white"/></a>

---

## Kit Bag

`Python` · `LLMs (GPT-4, Llama)` · `RAG` · `Fine-tuning (LoRA)` · `Weaviate` · `Neo4j` · `FastAPI` · `PostgreSQL` · `Redis` · `LightGBM` · `XGBoost` · `scikit-learn` · `Scrapy` · `FreeCAD` · `Docker`

---

## Currently

- 🧪 Teaching models to say "I'm not sure", the most underrated sentence in AI
- ✍️ Turning one more scary AI concept into something that finally makes sense
- 🌍 Looking for AI work where a wrong answer has real consequences, because that's where getting it right matters most

<sub>If you're building AI that people actually depend on, let's talk. If you're not sure your AI needs a human in the loop, let's definitely talk. </sub>
