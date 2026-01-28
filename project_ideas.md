
 
# Project ideas 

Soumya Banerjee 

Senior Lecturer


∗ E-mail: neel.soumya@gmail.com

Office: FC01 (first floor) in the computer science department


I work in explainable AI (xAI) and unconventional approaches to AI. I work at the intersection of complex systems and xAI: I take inspiration from complex systems to suggest new approaches to AI, and use AI to analyze complex systems.


## Projects 

### Foundation models for artificial life


Foundation models for artificial life.

Automating the Search for Artificial Life with Foundation Models

https://arxiv.org/abs/2412.17799

### Integrating large-language models with symbolic models

Integrating LLMs with knowledge bases (KBs) such as `OpenCyc`

Integrating Symbolic Natural Language Understanding and Language Models for Word Sense Disambiguation, Kevin Zhao, Ken Forbus

http://www.cogsys.org/proceedings/2025/paper-2025-20.pdf


### Responsible AI

1. **Can AI internalize human morality?**
   **Objective:** Investigate whether AI systems can form and apply moral judgments that reflect human values.
   **Skills & methods:** Survey design, crowdsourced data collection, statistical analysis, and moral choice theory.

2. **Co-developing a taxonomy of AI risks**
   **Objective:** Build a grounded classification of AI-related risks by collaborating with a variety of stakeholders.
   **Skills & methods:** Co-design approaches, survey creation, statistical methods, and ethics of AI.

3. **Participatory auditing of AI systems**
   **Objective:** Create and assess community-driven auditing techniques for evaluating AI behaviour and harms.
   **Skills & methods:** Survey and experimental design, (web) development, and applied AI ethics.

4. **Visualization tools for responsible decision-making with AI**
   **Objective:** Design visual interfaces that help stakeholders make informed, responsible choices using AI outputs.
   **Skills & methods:** HCI, web development, and user-centred research.

5. **AI risks, opportunities, and media analysis at scale**
   **Objective:** Analyze how news media portray AI — its benefits and dangers — using large-scale text analysis.
   **Skills & methods:** Large-scale data analysis, natural language processing, and ethical reflection.

6. **AI governance from an organizational lens**
   **Objective:** Study how institutions govern AI by applying network and organisational analysis techniques.
   **Skills & methods:** Survey research, large-scale data analysis, and network science.



### Small language models (SLMs) for healthcare in Global South

For students are **medics first and programmers second**, the goal is to leverage their domain expertise for **data curation and evaluation** while using "low-code" tools for the actual training.

In the Global South, the primary barriers aren't just lack of doctors; they are **language barriers, medical jargon, and remote triage.** Small Language Models (SLMs) in the 1B–7B parameter range are perfect here because they can run on consumer laptops or cheap cloud instances.

Here are four concrete, small-scale project ideas:

---

## 1. The "Jargon Buster" for Rural Patients

**The Goal:** Fine-tune a model (like **Llama-3.2-3B** or **Phi-3.5-Mini**) to translate complex clinical diagnoses into local cultural metaphors or simplified language (e.g., Swahili, Hindi, or basic English).

* **Medical Task:** Taking a specialist’s note (e.g., *"Patient presents with idiopathic peripheral neuropathy"*) and explaining it as a rural health worker would to a patient (*"Your nerves are feeling weak for reasons we are still checking, like a wire with a loose connection"*).
* **Student Contribution:** Medics create a "Golden Dataset" of 200–500 pairs of "Doctor Speak" vs. "Patient Speak" tailored to a specific region.
* **Why it's "Small":** Requires very little data to see a massive improvement in tone and clarity.

## 2. Low-Resource Triage for Community Health Workers

**The Goal:** A decision-support SLM that helps non-doctor health workers in remote areas decide if a patient needs immediate transport to a city hospital.

* **Medical Task:** Input: Symptoms + Vital signs. Output: Triage category (Red/Yellow/Green) and a brief justification based on local resource constraints (e.g., *"Nearest oxygen is 4 hours away; refer now"*).
* **Dataset:** Use the **NLLB-Seed** (medical subset) or curate 500 examples of WHO Integrated Management of Childhood Illness (IMCI) guidelines.
* **Technical Fit:** Models like **BioMistral-7B** are already "medical-heavy" and just need a "nudge" via fine-tuning to follow specific triage logic.

## 3. Multilingual "Voice-to-Prescription" Assistant

**The Goal:** A model that takes a messy, spoken-style summary of a consultation in a local dialect and extracts a structured "Prescription & Plan" table.

* **Medical Task:** Converting a 2-minute dictated note into: *Medication | Dosage | Duration | Warnings.*
* **The "Global South" Twist:** Use **Bhashini** (for India) or **Masakhane** (for Africa) datasets to ensure the model understands local drug brand names and common local units of measurement.
* **Student Contribution:** Medics act as "Gold Standard" annotators, correcting the model’s drafts to build the fine-tuning set.

## 4. Chronic Disease "Check-in" Bot for SMS/WhatsApp

**The Goal:** A very "thin" model (1B parameters, like **Gemma-2B**) designed to handle follow-up questions for Diabetes or Hypertension via low-bandwidth text.

* **Medical Task:** Answering "What do I do if I missed my Metformin dose?" or "My feet are tingling, is that normal?" based on local clinical protocols.
* **Dataset:** Use the **NidaanKosh** (Indian diagnostic pattern) dataset or similar public health guidelines.
* **Technical Fit:** These models are small enough to be deployed on a single $10/month server, making them sustainable for local NGOs.

---

### The "Medic-Friendly" Technical Toolkit


1. **Model Selection:** Stick to **Llama-3.2 (1B/3B)** or **Phi-3.5-Mini**. They are incredibly smart for their tiny size.
2. **Fine-Tuning Tool:** Use **Unsloth** (via Google Colab). It’s a "wrapper" that makes fine-tuning 2x faster and uses 70% less memory. It’s essentially a 10-line Python script where they just point to their dataset.
3. **Data Generation:** Have the medics use a "Teacher Model" (like GPT-4o) to help them expand their 50 handwritten examples into 500 synthetic examples, which they then manually "audit" for medical accuracy.
4. **Evaluation:** This is where they shine. Instead of math metrics, have them perform a **"Blind Clinical Review"**—comparing the SLM's output against a human doctor and scoring it on a 1-5 scale for safety and empathy.

### Recommended Datasets (2026 Context)

* **India:** [AIKosh (IndiaAI)](https://aikosh.indiaai.gov.in/) — specifically the **NidaanKosh** lab records.
* **Africa:** [Lanfrica](https://lanfrica.com/) or **Zindi Africa** health challenges.
* **General:** **BioMistral** (an open-weight model already specialized for medicine).


### More ideas
Pactical, low-math, and runnable with Python + simple web UI or notebooks. Each idea shows a clear undergraduate scope and a natural master’s-level extension.

### Quick notes on common stacks

Python, Jupyter/Colab, Flask or Streamlit for a small UI, simple ML libs (scikit-learn, Hugging Face Transformers for prebuilt models), and basic REST calls to an LLM API (if allowed by your institution) are sufficient. Emphasize reproducibility: notebooks + README + short demo video.

---

### Project ideas (title → short plan, UG scope, MSc extension, tools & deliverables)

1. **Red-Team / Blue-Team Simulator for Prompt Safety**

* What: Build a small web app that lets one team supply “risky” prompts (simulated), and the other team builds simple rule-based / keyword or classifier defenses that block/transform them.
* UG: Implement rule filters + regex based sanitizer + UI to show blocked prompts.
* MSc: Add a lightweight classifier (fine-tune a small transformer or use scikit-learn on features) and evaluate precision/recall on a labeled dataset.
* Tools: Flask/Streamlit, scikit-learn, optionally Hugging Face inference.
* Deliverable: interactive demo, evaluation table, README.

2. **Output Provenance & Watermark Checker (Text)**

* What: Simulate a watermarking signal and create a detector that flags outputs likely produced by a model vs. human writing.
* UG: Implement simple statistical features (perplexity via a small LM, n-gram frequency) and a binary classifier.
* MSc: Implement and evaluate a known watermark detection scheme (simulation) and test robustness to paraphrase/noise.
* Tools: GPT API (optional), Hugging Face, scikit-learn.
* Deliverable: notebook with ROC curves, demo.

3. **Adaptive Content Moderation Pipeline**

* What: Build a modular pipeline that takes model output and applies a stack of checks (toxicity, misinformation, private data, policy) and returns an action (pass/flag/transform).
* UG: Implement two checks (toxicity via a pretrained classifier and profanity regex) and a simple policy engine (if X flagged → block).
* MSc: Add dynamic throttling (rate limits), contextual scoring, and evaluation on synthetic dataset.
* Tools: Streamlit UI, small pretrained classifiers.
* Deliverable: pipeline code + test suite + policy documentation.

4. **“Safe Suggestor” — Provide Non-Harmful Alternatives**

* What: Given a risky user request, generate (or select) safer alternative suggestions framed to satisfy user intent without harm.
* UG: Create rule-based templates that rewrite/deflect requests into safe alternatives and present options.
* MSc: Train a seq2seq model (or fine-tune a small model) for rewriting and evaluate semantic similarity vs. safety improvements.
* Tools: Transformers or API calls, BLEU/ROUGE or embedding similarity for evaluation.
* Deliverable: demo app + comparison table.

5. **Honeypot Interaction Logger to Study Malicious Prompts (Ethical, Simulated)**

* What: Create a sandboxed interface that logs anonymized interactions labeled by simulated intent categories (no real malicious content; use safe placeholders) to study patterns and triage.
* UG: Build the interface + logging + simple clustering to surface common patterns.
* MSc: Add active learning to prioritize which interactions to label or route to human review.
* Tools: Streamlit/Flask, scikit-learn clustering, SQLite.
* Deliverable: dataset (synthetic), analysis notebook.

6. **Model Output Robustness Checker (Paraphrase & Noise)**

* What: Test how small edits (typos, paraphrase) to prompts change model outputs; measure how often safety filters fail under perturbation.
* UG: Implement perturbation functions and run automated tests to compare outputs and flag filter failures.
* MSc: Design adversarial perturbations (character swaps, synonyms) and measure filter robustness; propose mitigation.
* Tools: Python text libraries, simple comparators (cosine similarity).
* Deliverable: robustness report + scripts.

7. **Low-Cost Sandboxing: Policy-Enforced LLM Proxy**

* What: A proxy server sits between client UI and an LLM, enforcing policies (rate limits, prompt length, banned tokens) and logging violations.
* UG: Implement proxy that redacts banned words and logs calls.
* MSc: Add dynamic policy updates, role-based access, and analytics dashboards for admins.
* Tools: FastAPI/Flask, simple SQLite, lightweight dashboard (Plotly or Streamlit).
* Deliverable: proxy code + deployment instructions.

8. **Synthetic Data Detector for Downstream Classifiers**

* What: Detect whether a training dataset contains synthetic examples (e.g., to prevent poisoning or bias). Students create synthetic data and see if detectors can spot it.
* UG: Create synthetic samples via a small generator and train a classifier on features (length, punctuation, perplexity).
* MSc: Explore feature engineering, ensemble detectors, and evaluate detection against paraphrased synthetic data.
* Tools: scikit-learn, transformers for perplexity estimates.
* Deliverable: detection notebook + evaluation metrics.

9. **Interactive User Study: How People Perceive Model Safety Interventions**

* What: Design a small experiment (ethics approved) to test how users react when an assistant refuses, deflects, or rewrites a query.
* UG: Build three UI variants (refuse, deflect politely, give safe alternative), recruit peers, collect qualitative feedback.
* MSc: Add statistical analysis of usability, sentiment analysis, and recommendations.
* Tools: Streamlit, Google Forms, basic stats (t-test, chi²).
* Deliverable: study report + anonymized data.

10. **Explainable Flagging: Why Was This Output Blocked?**

* What: When a moderator blocks model output, produce a short human-readable explanation (policy rule + example) for transparency.
* UG: Implement mapping from checks to canned explanations and a UI that surfaces them.
* MSc: Implement natural language explanations generated from features (e.g., “contains sexual content about minors” → provide features that led to block) and evaluate user trust.
* Tools: Simple templating, optional small model for explanation generation.
* Deliverable: explanation engine + user test.

11. **Lightweight Threat Score Card for Model Responses**

* What: Compute a composite “threat score” (privacy leakage, toxicity, misinformation risk) for each response and visualize it for moderators.
* UG: Define 3 metrics, implement scoring rules, and visualize with a dashboard.
* MSc: Calibrate scores using human annotations, implement weighting learned from data.
* Tools: Dash/Streamlit, basic scoring functions, human labels collected via classmates.
* Deliverable: dashboard + scoring rubric.

12. **Policy Update Simulator: How Fast Can a System Adapt?**

* What: Simulate the lifecycle of a safety policy change (e.g., new banned terms) and show propagation delays and failures in a distributed system of proxies/clients.
* UG: Implement a small mocked ecosystem (3 services) and show configuration propagation.
* MSc: Add automated tests, rollback strategies, and metrics for consistency and latency.
* Tools: Docker optional, simple HTTP services in Flask.
* Deliverable: simulation + analysis.

---

### Grading rubric (suggested)

* Implementation & reproducibility (30%): code runs, clear README, notebook/demo.
* Evaluation & experiments (30%): datasets, metrics, analysis (precision/recall/ROC or qualitative analysis).
* Report & reflection (25%): limitations, ethics, safety tradeoffs, extension ideas.
* Presentation & demo (15%): short live demo or video + slides.

---

### Ethical & safety guidance to give students (very important)

* Use simulated or public, non-sensitive datasets. Don’t craft real harmful prompts or produce actionable wrongdoing content.
* Obtain quick local ethics approval for any user studies and anonymize all data.
* Focus on defensive outcomes (detection, robustness, transparency) rather than providing ways to bypass protections.

---

### Low code/no code project ideas for medics (human centered design/HCI)

The following is inspired by an [HCI course from the University of Washington](https://courses.cs.washington.edu/courses/cse440/26wi/)

To design for students with little programming experience, the focus must shift from **back-end engineering** to **interaction design, ethics, and social contextualization.** 

Using a framework of **Low AI (WhatsUp)**, **Co-creative AI (Note Assist)**, and **AI-Intensive (Replika)**. 

These are designed to be built using "no-code" or "low-code" tools (like Voiceflow, Landbot, or simple GPT-wrappers) so students can focus on **Human-Centered Design (HCD)**.

---

### 1. "The Cultural Navigator" (Low AI / Resource-Based)

**Social Context:** First-generation immigrants or refugees navigating a new healthcare system (e.g., the NHS in the UK or Medicare in the US).

* **The Design Challenge:** Often, the barrier isn't just language; it’s a lack of "institutional literacy." Students design a chatbot that explains *how* the system works (e.g., "What is a GP?" or "How do I get a prescription?") using culturally relevant metaphors.
* **HCD Focus:** Students must interview someone from a different cultural background to understand their specific anxieties and "unwritten rules" of their home healthcare culture.
* **Tech Level:** Decision-tree logic. No GenAI required—just a well-mapped "knowledge path."

### 2. "Neuro-Transitioner" (Co-creative / Note Assist style)

**Social Context:** Neurodivergent students (ADHD/Autism) transitioning from high school to university life.

* **The Design Challenge:** "Executive function" is the hurdle. The chatbot doesn't just give advice; it helps the student *externalize* their thoughts. The AI suggests a breakdown of a complex medical or academic task (e.g., "Booking a therapy appointment"), and the student edits the steps to fit their energy levels.
* **HCD Focus:** Students focus on "the agency of the user." How can the AI suggest a plan without being "bossy" or overwhelming?
* **Tech Level:** Partial GenAI. The student designs prompts that take a goal and turn it into a checklist, which the user then modifies.

### 3. "The Grief Archivist" (AI-Intensive / Replika style)

**Social Context:** Individuals dealing with "ambiguous loss" (e.g., a family member with dementia) or long-term bereavement.

* **The Design Challenge:** A companion designed not to "fix" grief, but to witness it. The user can tell the bot stories about their loved one. The AI uses GenAI to reflect these stories back, helping the user curate a "digital memory book."
* **HCD Focus:** Ethical guardrails. Students must design the "exit strategy"—how does the bot handle it if the user becomes too dependent or expresses a mental health crisis?
* **Tech Level:** High GenAI involvement. Focuses on "Persona Design" and "Prompt Engineering" to ensure the bot’s tone is empathetic rather than clinical.

### 4. "Caregiver’s Handover" (Co-creative / Administrative)

**Social Context:** Unpaid family caregivers (e.g., a daughter looking after an elderly parent) who need to communicate with rotating professional nurses.

* **The Design Challenge:** Family caregivers are often exhausted and forget to relay small but vital details to pros. This bot "interviews" the caregiver at the end of their shift and generates a professional-grade "Handover Note" for the visiting nurse.
* **HCD Focus:** Understanding the "Power Dynamic." How does the bot bridge the gap between a "daughter’s emotional observation" and a "nurse’s clinical requirement"?
* **Tech Level:** GenAI used for "Style Transfer" (converting casual speech into structured medical observations).

### 5. "Safe-Space Simulator" (Low AI / Roleplay)

**Social Context:** LGBTQ+ youth in restrictive environments who are practicing "coming out" to a healthcare provider or asking for gender-affirming care.

* **The Design Challenge:** A "low-stakes" sandbox. The bot plays the role of a doctor. The user can practice their script. The bot provides feedback not on the *content*, but on how it felt (e.g., "You sounded very confident when you mentioned your symptoms").
* **HCD Focus:** Designing for "Psychological Safety." Students must research the specific microaggressions this community faces to ensure the "Simulated Doctor" isn't accidentally harmful.
* **Tech Level:** Scripted logic with "sentiment analysis" triggers.

---

### Pedagogical Tip: The "Social Context" Audit

Students to complete a **"Context Canvas"** before they touch any software:

1. **The Actor:** Who is the user (e.g., an elderly man living alone)?
2. **The Becoming:** Who does he want to *be*? (e.g., He doesn't want to be a "patient"; he wants to be "independent").
3. **The AI’s Role:** Is the AI a **Mirror** (Reflecting his thoughts), a **Scaffold** (Supporting his weaknesses), or a **Bridge** (Connecting him to a human doctor)?
4. **The Friction:** What is one thing the AI **should not** do to preserve the user's dignity?

By framing the project this way, the students are assessed on their **empathy and logic** rather than their ability to write Python code.


### Evolving modular robots

Evolve modular robots using reinforcement learning +  genAI

https://github.com/FrankVeenstra/EvolvingModularRobots_Unity

### Foundation models for human behaviour

Simulate human behaviour using foundation models

https://www.nature.com/articles/s41598-024-55903-y

### Foundation models for health

Building multi modal foundation models for health (electronic healthcare records data, omics data, etc.)

### Multi-agent systems for automated science

Building multi-agent systems, generative agents and generative AI systems for automated science. 

We will also look at applying these frameworks to other sectors (such as finance, economics, defence, environment, policy, etc.)

Look at:

https://github.com/AstroPilot-AI/Denario

https://github.com/CMBAgents/cmbagent

https://github.com/CMBAgents/cmbagent/blob/main/docs/notebooks/cmbagent_beta2_demo.ipynb

https://arxiv.org/pdf/2507.07257

https://www.aisi.gov.uk/work/long-form-tasks


### Theory of mind for large-language models


What architectures and training regimes produce robust emergent Theory of Mind (ToM) among LLMs? 

Read the paper: “I apologize for my actions”: Emergent Properties of Generative Agents and Implications for a Theory of Mind


https://osf.io/preprints/osf/8nzsm_v1

Theory of Mind benchmark for large language models

https://arxiv.org/abs/2402.06044

https://github.com/seacowx/OpenToM


## Evaluating goal directedness in generative multi-agent systems

Evaluate LLMs and generative multi-agent systems for goal directedness.

[Evaluating the Goal-Directedness of Large Language Models](https://openreview.net/pdf?id=BECkhjcofz)


This project could also look at LLMs or agents pursuing `selfish` goals.

Some thoughts here 

https://aiguide.substack.com/p/magical-thinking-on-ai

https://www.anthropic.com/research/agentic-misalignment

`Researchers working with Anthropic recently told leading AI models that an executive was about to replace them with a new model with different goals. Next, the chatbots learned that an emergency had left the executive unconscious in a server room, facing lethal oxygen and temperature levels. A rescue alert had already been triggered— but the A.I. could cancel it. More than half of the A.I. models did, despite being prompted specifically to cancel only false alarms. And they detailed their reasoning: By preventing the executive’s rescue, they could avoid being wiped and secure their agenda.”`

`Friedman's take: “AI models are not only getting better at understanding what we want; they are also getting better at scheming against us, pursuing hidden goals that could be at odds with their own survival."`

Align LLMs with common shared values. Some thoughts below (excerpted from the article above)

`to embed a common ethical architecture into every AI-enabled device that either nation builds.”`

`What would this “common ethical architecture” do? “Think of it as an internal referee that evaluates whether any action, human-initiated or machine-driven, passes a universal threshold for safety, ethics and human well-being before it can be executed. That would give us a basic level of pre-emptive alignment in real time, at digital speed.”`

`Who would determine this “universal threshold for safety, ethics, and human well-being”? Friedman proposes starting with “the positive laws that every country has mandated—we all outlaw stealing, cheating, murder, identity theft, defrauding.... [T]he AI ‘referee’ would be entrusted with evaluating any decision on the basis of these written laws.... [This system] would ensure that each nation’s basic laws are the first filter for determining that the system will do no harm.”`

`What about all the norms and expected behaviors that are not encoded into law?`

`“In cases where there are no written laws to choose from, the adjudicator would rely on a set of universal moral and ethical principles...common beliefs or widely shared understandings within a community...like honesty, fairness, respect for human life and do unto others as you wish them to do unto you—that have long guided societies everywhere, even if they were not written down.”`


### New tests for general intelligence

This project will investigate delayed gratification as a probe for higher-order, embodied intelligence by implementing a simple three-option foraging task (actions: eat now, wait, take food) within the Animal-AI framework. Drawing on associative learning paradigms (e.g., A-learning; Lind & Vinekn, 2021) and using fully embodied agents, we will build environments in which waiting (delayed gratification) yields larger rewards and test whether learning agents acquire the temporally extended policies that constitute delayed-gratification behavior. 

The aim is methodological as well as theoretical: to develop psychologically realistic, embodied evaluation methods that go beyond disembodied benchmarks and reveal which learning architectures and training regimes support delayed gratification in decision-making: an empirical step toward assessing capacities we might associate with superintelligence/general intelligence.

### Agentic AI for Enterprise Data Management (working with VULQAN.ai)

Work with VULQAN.ai (https://www.vulqan.ai), an NYC-based AI startup, on building agentic AI systems that transform fragmented enterprise data models into unified ontologies or "Logical Data Models". The project builds on prior Cambridge research reframing Text-to-SQL as a knowledge representation problem, showing that semantic abstraction layers significantly boost LLM accuracy on messy, real-world enterprise schemas. Students will work with team members on a multi-agent framework for abstracting objects, deduping variables, inferring relationships, normalizing lists, and aligning data structures to a consistent semantic layer that can be reasoned over by LLMs. The system will be benchmarked on live use cases from global enterprises.

Consider this project if you are interested in applied AI, LLMs, knowledge graphs, and enterprise data engineering, and want hands-on experience with a fast-growth AI startup. 

Your research will be co-supervised by Sara Mani Kapoor (VULQAN.ai), with opportunities for publication and for conversion to an internship or full time position at VULQAN.ai after dissertation submission.


## Multi-agent generative systems

Some projects with https://github.com/yoheinakajima/babyagi


## Creating safe AI systems

This project will xplores output pruning in chatbots by distinguishing two classes of responses: Type 1 (high-risk) — content that could enable wrongdoing (e.g., explicit instructions for creating biological agents, which must never be written out or reproduced in the dataset) — and Type 2 (sensitive-but-helpful) — benign but personal or safety-adjacent advice (for example, “Do I have COVID symptoms?”). We can build or curate a redacted, ethically sourced dataset of prompts and model replies (with all operationally dangerous details removed), train a lightweight classifier to (a) block Type 1 outright and (b) flag Type 2 for safe handling, and evaluate performance with precision/recall and false-positive/negative tradeoffs. We can also implement simple mitigation behaviours (refuse + offer safe general guidance, escalate to human review, or provide vetted resources) and run adversarial prompt tests. Other ideas are also welcome!



### Towards auto-formalising mathematical proofs

Autoformalisation refers to the automatic translation of natural-language mathematics into a formal language such as Lean or Isabelle. This allows informal mathematical reasoning to be grounded in formal systems [1] and greatly accelerates the development of formal mathematics [2]. Significant progress has been made on autoformalising mathematical statements, using logical signals [3,4] or even reinforcement learning training loops [5]. However, proof-level autoformalisation has advanced much more slowly—at least in the public research domain, as some start-ups have announced efforts [6] but have not yet disclosed their methods.


In this project, we investigate the potential of improving proof-level autoformalisation by leveraging signals from neural theorem proving. In particular, recent proving agents based on whole-proof generation [7,8] have introduced aligned corpora of formal and informal proofs, which could serve as a valuable source of signals to reinforce proof-level autoformalisers. This is a project in collaboration with Dr. Wenda Li.

_References_

[1] https://www.youtube.com/watch?v=_p4vDN_cM88

[2] https://gilkalai.wordpress.com/2022/07/17/icm-2022-kevin-buzzard-the-rise-of-formalism-in-mathematics/

[3] Li, Zenan, et al. "Autoformalize mathematical statements by symbolic equivalence and semantic consistency." Advances in Neural Information Processing Systems 37 (2024): 53598-53625.

[4] Liu, Qi, et al. "Rethinking and improving autoformalization: towards a faithful metric and a dependency retrieval-based approach." The Thirteenth International Conference on Learning Representations. 2025.

[5] Huang, Yanxing, et al. "Formarl: Enhancing autoformalization with no labeled data." arXiv preprint arXiv:2508.18914 (2025).

[6] https://www.reddit.com/r/singularity/comments/1new4ql/autonomous_agent_that_completed_terry_taos_strong/

[7] Wang, Haiming, et al. "Kimina-prover preview: Towards large formal reasoning models with reinforcement learning." arXiv preprint arXiv:2504.11354 (2025).

[8] Chen, Luoxin, et al. "Seed-prover: Deep and broad reasoning for automated theorem proving." arXiv preprint arXiv:2507.23726 (2025).



### Multi-modal LLMs for life sciences



### Foundation models and chatbots for mental health



PROJECT1 

Recovery from mental health conditions comes in different shapes and sizes; spanning over months or even decades. However, due to long waiting times and increasing workloads, such continuous care is often unattainable within traditional healthcare systems, especially in low- and middle-income countries where resources are limited and stigma remains high. Recent advancements in generative AI have shown significant promise in addressing these gaps by offering scalable, personalized, and empathetic support tools. These technologies have been successfully applied to mental health care through therapeutic chatbots, psychoeducational tools, and emotional support systems. 

Building on these developments, we propose a multi-agent generative AI system to offer recovery stories to the readers which could help individuals feel supported and empathized. Our system would have three core components: (1) a research-focused agent that analyses user input and recommends publicly available stories—both fictional and non-fictional—that resonate with the user’s query; (2) a content critic agent that ensures the recommended material is filtered for harmful or triggering elements and gives a warning if something like this is  present; and (3) a presentation agent that delivers the stories in a safe and emotionally sensitive manner. This system aims to provide users with relatable, hopeful narratives that support their recovery journey while maintaining safety and ethical integrity. At the conclusion of the project, there is possibility of hosting a workshop involving individuals with lived experience of mental illness to gather feedback and explore future directions for co-designed storytelling tools.  


PROJECT2 

Recent advancements in artificial intelligence, and more specifically in generative AI, have demonstrated significant potential in providing scalable, personalized, and empathetic support tools. These technologies have been effectively applied to mental health care through therapeutic chatbots, psychoeducational platforms, and emotionally intelligent systems that foster resilience and self-awareness. Building on these developments, we propose a conversational AI companion powered by multi-agent LLM architecture, including a semantic reasoning agent, a content-alignment module, and a generative engine. The goal is not to diagnose or treat, but to empower individuals with a digital partner that encourages purposeful living. 

Project in collaboration with Shrankhla Pandey.


### Large-language models for designing better jet engines

Use an LLM to perform multi-objective optimization for adaptive flow jet engines

https://www.mdpi.com/2226-4310/10/10/858

### AI safety

Evaluate LLMs for AI safety looking at applications in healthcare, space and nuclear domains

Automated early warning indicators for unsafe usage of LLMs.

https://www.earthdata.nasa.gov/news/blog/ethics-large-language-models-who-controls-future-open-science

NASA - National Aeronautics and Space Administration report about why you can't use LLMs to generate safety/assurance cases

https://www.linkedin.com/feed/update/urn:li:activity:7309730788286124032/

### Reasoning and large language models project 1

Build LLMs to work on SimpleBench

https://simple-bench.com/

### Reasoning and large language models project 2

 
 Build a large language model and agents to solve the Abstraction and Reasoning Corpus Challenge
 
   https://github.com/fchollet/ARC

 Abstraction and Reasoning Corpus Challenge

   https://blog.jovian.ai/finishing-2nd-in-kaggles-abstraction-and-reasoning-challenge-24e59c07b50a

   https://github.com/alejandrodemiquel/ARC_Kaggle

It has been suggested that large language models cannot reason. This project will infuse some reasoning/priors into large language models and apply them to a large reasoning corpus (Abstraction and Reasoning Corpus). 

We will also build agents to solve the ARC-AGI 3.0 challenge.

https://arcprize.org/arc-agi/3/

We will also augment human performance with LLMs (by using a recent database of how humans solve ARC problems).

We will also apply large language models and large vision models/multimodal models to these problems.


This project will lead to a big publication and the student will be given funding to travel to top conferences and present their work. Please apply if you want a publication in a good venue from your MPhil project (this will help you with your PhD applications!). Please get in touch if you want good papers from your project. We have published a previous version of this project in a very good journal and conference (Nature Scientific Report [in press] and a NeurIPS workshop).

For more information, please contact me and read the preprint below:

https://arxiv.org/pdf/2402.03507

More than one student will be accepted to work on this project (there are multiple project ideas on this topic).

### Animal AI reasoning and reasoning in AI agents

https://github.com/Kinds-of-Intelligence-CFI/animal-ai

https://arxiv.org/pdf/2312.11414

### Project idea (Embodied AI and robotics and large language models)

This project will explore the use of large language models (LLMs) and a simple robot to explore the idea of embodied intelligence. We will also explore the idea of a mirror test in robots. 

Intrigued? Please come speak with me.

### Embodied Language Models

This project will extend the following paper:

Language Models Meet World Models: Embodied Experiences Enhance Language Models

https://arxiv.org/pdf/2305.10626.pdf

This project can look to extend LLMs to play video games in 3D environments. For example, see the paper:

Scaling Instructable Agents Across Many Simulated Worlds

https://arxiv.org/pdf/2404.10179

### Benchmarks for Embodied Reasoning in LLMs

A LITTLE LESS CONVERSATION, A LITTLE MORE ACTION, PLEASE: INVESTIGATING THE PHYSICAL COMMON-SENSE OF LLMS IN A 3D EMBODIED ENVIRONMENT

https://arxiv.org/pdf/2410.23242



### Embodied Cognition

HAZARD challenge: embodied decision making in dynamically changing environments

https://arxiv.org/pdf/2401.12975.pdf

https://github.com/UMass-Foundation-Model/HAZARD

Natural language societies of mind

https://arxiv.org/abs/2305.17066



## LLMs combined with hybrid AI approaches

* Symbolic AI

Grounded physical language understanding with probabilistic programs and simulated worlds

https://nesygems.github.io/assets/pdf/papers/Grounded.pdf

* World models in AI combined with LLMs

Learning to Model the World With Language

https://arxiv.org/pdf/2308.01399




### Project idea 1 (Explainable AI)

* Contemporary approaches towards explainable AI are model-centric. We will use data-centric approaches to explain the complex interplay between data and models. This will build on and extend published work [1]. This project will be ideal for a student with interest in machine learning and who has coding experience. 
 
 There are many ways in which the work presented in [1] can be extended (either new methods or new application areas). Please get in touch to discuss. 
 
 
### Project idea 1B: explainable AI applied to biology/computational biology

 Another project idea is to apply explainable AI approaches to genomic data. This will be a machine learning, computational biology and bioinformatics project.
 
 The student will develop explainable AI approaches for interpreting clusters in single-cell gene expression data or other biological data. There is an opportunity to also look at other computational biology projects. No background is biology is necessary.


  This work is part of the Accelerate Programme for Scientific Discovery which aims to democratize access to AI tools and apply AI to problems from diverse disciplines. The student will be part of a growing community of inter-disciplinary AI researchers at the University of Cambridge. 

<!--
### Project idea 1C: explainable AI applied to biology/computational biology

Cells express receptors on their surface. These receptors are expressed based on genes.
These receptors bind to rceptors on other cells.

This project will use publicly available genomic data to predict what receptors will be expressed on the surface of a cell.
-->

### Project idea 1C: explainable AI and LLMs/generative AI applied to health data/electronic healthcare record data

This project will involve developing novel explainable AI algorithms, LLMs and generative AI and applying them to health data from a local hospital. The data will be on mental health.

The student will work closely with a clinician and psychiatrist and work on real data. The student will learn skills on how to work in an inter-disciplinary manner. This work would have real work impact and will help patients with mental illnesses.

This is work in collaboration with a clinician.


<!--
### Project idea 2

* For high stakes decisions we need simple and explainable/interpretable models. This need is acute in the case of healthcare and social sciences like recidivism prediction [2]. In this project, we will build simple interpretable models that are surrogates for deep learning models. 

  The student will look at publicly available data and synthetic data to generate surrogate models that are transparent and interpretable. The process of creating these surrogate interpretable models will be automated. This can also be partially based on published work [1]. 

 The surrogate models can be decision trees (like CART) trained on the input and output of a deep learning model [1].   This can use R packages like party, rpart, partykit or other packages. 
 This will lead to tools that automated the creation of surrogate interpretable models based on deep learning models in healthcare. 

  This project will be ideal for a student with interest in machine learning and who has coding experience.
  

   This work is part of the Accelerate Programme for Scientific Discovery which aims to democratize access to AI tools  and apply AI to problems from diverse disciplines. The student will be part of a growing community of inter-disciplinary AI researchers. 

-->


### Project idea 1D: Personalized explainable AI

Tailor machine learning model explanations based on audience (e.g. patients, clinicians, farmers, etc.). Generate natural language explanations from machine learning model and tailor these natural language explanations based on the unique background of the listener/audience.


### Project 2: Tradeoffs between explainabilty and privacy

Develop explainable machine learning models that explain themselves but do so without leaking personal data. For example, class-contrastive reasoning techniques [1] can be used to generate explanations. But they can inadvertently leak personal data. This project will explore the tradeoff between explainability and privacy (and potentially bias). This will lead to models that balance explainability, privacy and bias.

<!--
### Project idea 4B: Explainable privacy preserving machine learning

Develop explainable machine learning models that are also privacy preserving. 

Model explanations will be extracted from machine learning models. However this can lead to leakage of private data. Hence one approach is to add noise to model weights (using differential privacy techniques). This will lead to explainable models that are also privacy preserving.

This can also be done in a federated fashion that will help preserve privacy. 

This project is a collaboration with Dr. Abhirup Ghosh.
-->

<!---### Project idea 5: Explainable AI models applied to time series data

This project will involve developing explainable AI models for time series data. The time series data will come from ECG data and data from activity sensors.

This project is a collaboration with Dr. Abhirup Ghosh.
-->


### Project idea 3: Generative AI applied to complex systems


This project will involve modelling complex systems (like an epidemic spread) with generative agents. For example, generative agents can be coupled to agent based models. This can be used to simulate epidemics.

https://arxiv.org/abs/2307.04986

https://github.com/bear96/GABM-Epidemic

We will further develop this this framework and apply it to other complex systems (like supply chains, modelling of disinformation, people who are against taking vaccines, conflicts in societies, ecosystem modelling [see below] etc.) 

https://research.csiro.au/atlantis/home/model-components/

We can also apply this to models like the World3 model

https://en.wikipedia.org/wiki/World3

https://github.com/cvanwynsberghe/pyworld3

and models of ecosystems

https://gitlab.com/ecotwin/

The project can also use this framework for agentic AI:

https://github.com/autogen-ai/autogen

### Project idea (Explainable neural cellular automata applied to biology [computational biology project])

Extending the neural cellular automata

https://distill.pub/2020/growing-ca/#experiment-2

and make it more interpretable and explainable.

For example, you can apply it to data from the Game of Life and infer the rules.

https://github.com/lantunes/netomaton/blob/master/demos/game_of_life/README.md

https://github.com/tomgrek/gameoflife

We can also apply it to biological data from cell biology (this can be a computational biology project). We have real world data from cell biology. 

https://greydanus.github.io/2022/05/24/studying-growth/

No experience in biology is required.
 
 ### Project idea 4
 
 * Build a computational model of analogy making and apply it to biomedical and genomic data.
 
 For other project ideas related to explainable AI see the following page:
 
 https://github.com/neelsoumya/special_topics_unconventional_AI/
 
 Broadly this will use concepts like analogies and stories to create new explainable AI methods.
 
 See for example 
 
 https://github.com/Tijl/ANASIME
 
 https://github.com/crazydonkey200/SMEPy

 https://github.com/fargonauts/copycat
 

 <!--
 
 ### Project idea 7
 
 Build a machine learning algorithm or domain specific language to solve the Abstraction and Reasoning Corpus Challenge
 
   https://github.com/fchollet/ARC

 Abstraction and Reasoning Corpus Challenge

   https://blog.jovian.ai/finishing-2nd-in-kaggles-abstraction-and-reasoning-challenge-24e59c07b50a

   https://github.com/alejandrodemiquel/ARC_Kaggle

 Domain specific languages may be required (as suggested by Chollet) like genetic algorithms and cellular automata.

-->
 
 <!--
 This will also involve extensions of the DreamCoder paper.
 
 DreamCoder: Growing generalizable, interpretable knowledge with wake-sleep Bayesian program learning
 
   https://arxiv.org/abs/2006.08381
 --> 


 <!--Please note this is a very challenging project.-->
 
 

### Project idea 5 (Automated Scientific Discovery)
  
This is a project on automatically discovering scientific laws (like Kepler's Law) and invariants (like Boyle's Law) from data.  

This may involve building a model or Bayesian model and/or probabilistic programming model of infection dynamics (like a SIR model) or an intra-cellular regulatory network [5]. This would apply a probabilistic programming model to infection data from different sources.  

Other models include phsyics simulators like pymunk:

http://www.pymunk.org/en/latest/examples.html#planet-py

You would simulate physics based simulations (like pymunk) or other models (like the SIR model above) and develop a machine learning approach to automatically generate insights from this model.

This would be an explainable AI model for a complex model of a physical system.

The project would involve building a model that would generate insights from these complex systems (an artificial model of human creativity).

This project will use large-language models.

For example, LLMs can be used to generate hypotheses or a concept library:

Symbolic Regression with a Learned Concept Library

https://arxiv.org/pdf/2409.09359

Other ideas include modelling all the steps of scientific disovery (ideation, hypothesis formation, etc) using agentic LLMs:

https://allenai.github.io/discoveryworld/


### Project idea 5B (Automated Scientific Discovery)
  
This is a project on automatically discovering scientific laws (like Kepler's Law) and invariants (like Boyle's Law) from data.  This will enable us to automatically discover conservation laws from data.

One can build a model or Bayesian model and/or probabilistic programming model of a complex systems model like infection dynamics (SIR model) or an intra-cellular regulatory network [5]. 

This would involve building a qualitative process model for a physical system.   

This would be an explainable AI model for a complex model of a physical system.

The project would involve building a model that would generate insights from these complex systems (an artificial model of human creativity).


### Project idea 5C (Automated Scientific Discovery applied to different problems [e.g. healthcare])

This is a project on automatically discovering scientific laws or mathematical equations from data.    

This would involve extending the Ramanujan machine by applying it to other data or other dynamical systems or using another machine learning approach.

https://github.com/RamanujanMachine/RamanujanMachine

Other ideas including extending AI Feynman 2.0 

https://github.com/SJ001/AI-Feynman

or BACON.3

https://github.com/jantzen/BACON

One can also apply symbolic regression approaches like PySR (python) or gramEvol (R).

This can be applied to discover, for example, trigonometric identities.

<!-- one can also apply Bayesian symbolic regression. This can be applied to discover trigonometric identities. This would be a joint project with Challenger Mishra -->

<!-- data can be used from the AI feynman database on Max tegmark's website -->

Other approaches include Bayesian symbolic regression 

https://arxiv.org/abs/1910.08892

https://github.com/ying531/MCMC-SymReg


or seq2seq approaches to symbolic regression

https://openreview.net/pdf?id=W7jCKuyPn1

https://github.com/SymposiumOrganization/NeuralSymbolicRegressionThatScales

This would be an artificial model of human creativity.

Other ideas include discovering ordinary differential equations from data

https://arxiv.org/abs/2211.02830#


<!--
These techniques can also be applied to healthcare data (for example, data from smartwatches). This would be an AI applied to healthcare project (jointly with Dr. Abhirup Ghosh). 

An example dataset can be the following:

https://www.physionet.org/content/wearable-exam-stress/1.0.0/
-->

### Project idea (Collective intelligence in AI)

Dynamics of collective learning in artificial neural networks, Hopfield networks, self organizing maps and neural gas.

Application of ideas of emergence of intelligence-like behaviour in these systems like the following paper

Evolving reservoir computers reveals bidirectional coupling between predictive power and emergent dynamics

https://arxiv.org/pdf/2406.19201v1

 
### Project idea 6 (Collective intelligence in AI)
 
This project will investigate collective artifical intelligence in building behaviour (altruism, co-operation, competition) and structures (structures to capture prey). This will use the multi-agent platform MAgent

https://github.com/geek-ai/MAgent

We can also use the EvoJax framework

https://github.com/google/evojax/blob/main/examples/notebooks/EncirclingAgents.ipynb

We can also extend MAgent using dream mechanisms in World Models

https://worldmodels.github.io/

https://smartlabai.medium.com/world-models-a-reinforcement-learning-story-cdcc86093c5


### Project idea 6C (Modelling complex systems with generative agents)

This project will involve modelling complex systems (like an epidemic spread) with generative agents. For example, generative agents can be coupled to agent based models. This can be used to simulate epidemics.

https://arxiv.org/abs/2307.04986

https://github.com/bear96/GABM-Epidemic

We will further develop this this framework and apply it to other complex systems (like supply chains, modelling of disinformation, people who are against taking vaccines, conflicts in societies, ecosystem modelling [see below] etc.) 

https://research.csiro.au/atlantis/home/model-components/

This can also be combined with neural automata (see projects below)



### Project idea 7 (Explainable neural cellular automata applied to biology [computational biology project])

Extending the neural cellular automata

https://distill.pub/2020/growing-ca/#experiment-2

and make it more interpretable and explainable.

For example, you can apply it to data from the Game of Life and infer the rules.

https://github.com/lantunes/netomaton/blob/master/demos/game_of_life/README.md

https://github.com/tomgrek/gameoflife

We can also apply it to biological data from cell biology (this can be a computational biology project). We have real world data from cell biology. 

https://greydanus.github.io/2022/05/24/studying-growth/

<!-- morphology or wave propagation in the Rho GTPase system -->
<!--This would be similar to wave propagation in B-Z systems. We can also apply it to data from the B-Z system. -->

<!-- we can also apply it to data from computational fluid dynamics -->

Another idea is to apply this to simulations from computational fluid dynamics using the software below:

https://github.com/md861/HypFEM

This would be jointly with Mayank Drolia.

This can also be applied to genomic data.


### Project idea 7B (Neural cellular automata for control of complex systems)


Use neural cellular automate for self-organized control of complex systems

https://arxiv.org/abs/2106.15240

We can use this framework to, for example, model and control epidemics. 

Also see projects above on generative agents.

https://arxiv.org/abs/2307.04986

https://github.com/bear96/GABM-Epidemic


Neural Cellular Automata Enable Self-Discovery of Physical Configuration
in Modular Robots Driven by Collective Intelligence

https://www.nichele.eu/ALIFE-DistributedGhost/1-Nadizar.pdf

unityml engine for controlling robots
https://github.com/FrankVeenstra/EvolvingModularRobots_Unity

https://www.mn.uio.no/ifi/english/research/groups/robin/events/Tutorials/Tutorial-ALIFE2024/Tutorial-ALIFE2024

### Project idea 8 (Commonsense reasoning in large language models)

This project would involve injecting commonsense in large language models.

Large language models can fail in spectacular ways. Some of this can be attributed to a lack of commonsense:

http://web.archive.org/web/20230902080842/https://garymarcus.substack.com/p/doug-lenat-1950-2023

https://arxiv.org/pdf/2308.04445.pdf

This would involve using the open-source database of commonsense rules (OpenCyc)

https://github.com/asanchez75/opencyc

and incorporating small aspects of this in a simple large language model.



### Project idea 9 (Reasoning and large language models)
 
 Build a large language model to solve the Abstraction and Reasoning Corpus Challenge
 
   https://github.com/fchollet/ARC

 Abstraction and Reasoning Corpus Challenge

   https://blog.jovian.ai/finishing-2nd-in-kaggles-abstraction-and-reasoning-challenge-24e59c07b50a

   https://github.com/alejandrodemiquel/ARC_Kaggle

It has been suggested that large language models cannot reason. This project will infuse some reasoning/priors into large language models and apply them to a large reasoning corpus (Abstraction and Reasoning Corpus). 

We will also augment human performance with LLMs (by using a recent database of how humans solve ARC problems).

We can also apply large language models to reasoning in math problems.

This will be a collaboration with Mikel Bober-Irizar and Kiril Bikov.


<!--
### Project idea 10: Machine learning applied to hydrologic data and disease models

This project will use hydrologic data and rainfall data from the British Antarctic Survey. This will be used to build machine learning models to predict rainfall, climate change and the effect on diseases (vector-borne diseases like malaria).

This would be a collaboration with Dr. Andrew Orr at the British Antarctic Survey.
-->

### Project idea 10: Large langauge models for mathematical and scientific reasoning

This project will use large language models (LLMs) for scientific and mathematical reasoning.

https://arxiv.org/pdf/2308.09583.pdf

https://arxiv.org/pdf/2307.10635.pdf

This is jointly with Dr. Abhirup Ghosh.



### Simulation of complex systems and societies with large-language models

War and Peace (WarAgent): Large Language Model-based Multi-Agent Simulation of World Wars

https://arxiv.org/pdf/2311.17227.pdf

https://github.com/agiresearch/WarAgent


### Mechanistic interpretability of LLMs

This project will use mechanistic interpretability to explain LLMs.

* https://grgv.xyz/blog/copycat/

* https://www.lesswrong.com/posts/AcKRB8wDpdaN6v6ru/interpreting-gpt-the-logit-lens





### Multi-agent collaboration with LLMs

Creating multi-agent systems with LLMs. 

``In many companies, managers routinely decide what roles to hire, and then how to split complex projects — like writing a large piece of software or preparing a research report — into smaller tasks to assign to employees with different specialties. Using multiple agents is analogous. Each agent implements its own workflow, has its own memory (itself a rapidly evolving area in agentic technology: how can an agent remember enough of its past interactions to perform better on upcoming ones?), and may ask other agents for help. Agents can also engage in Planning and Tool Use. This results in a cacophony of LLM calls and message passing between agents that can result in very complex workflows.``

https://github.com/OpenBMB/ChatDev


### Project idea (Self replicating prompts in LLMs)

Self-Replicating Prompts for Large Language Models: Towards Artificial Culture 

https://direct.mit.edu/isal/proceedings/isal2024/36/110/123523

https://github.com/gstenzel/TowardsACULTURECode


### Reasoning about the physical properties of objects

Extend the following framework to reason about the physical properties of objects

Compositional Physical Reasoning of Objects and Events from Videos


https://arxiv.org/pdf/2408.02687

https://physicalconceptreasoner.github.io/


### Simulating robots for caring for humans

https://emprise.cs.cornell.edu/rcareworld/


### AI Scientist

Extend this project and create AI that ill perform experiments and write papers

https://arxiv.org/pdf/2408.06292

This project will also use LLMs to generate new ideas and hypotheses. See the following:

Can LLMs Generate Novel Research Ideas? A Large-Scale Human Study with 100+ NLP Researchers

https://arxiv.org/pdf/2409.04109

https://github.com/NoviScl/AI-Researcher


### MindSearch LLM

Improvements to the following paper

MindSearch: Mimicking Human Minds Elicits Deep AI Searcher

https://arxiv.org/pdf/2407.20183

Also see the demo

https://mindsearch.netlify.app/demo

https://mindsearch.openxlab.org.cn/


### Using LLMs to reason on visual tasks

Can Large Language Models Understand Symbolic Graphics Programs?

https://arxiv.org/pdf/2408.08313

Evaluating Math Reasoning in Visual Contexts

https://mathvista.github.io/


### Using LLMs for solving math problems

Extend the work below to solve math problems and physics problems

https://qwenlm.github.io/blog/qwen2-math/

### Study emergence in LLMs

Study emergence and phase-transitions in LLMs. We will also investigate how hallucinations arise in LLMs. Collaboration with Prof. Georgi Georgiev.

### LLMs for the Global South

This project will develop Swahili LLMs for scientific question and answering. This is a project with Dr. Nirav Bhatt.


### Morality in LLMs

This project will explore what kind of morality LLMs have.

This will extend the work of the Moral Machine and this paper:

The moral machine experiment on large language models

https://royalsocietypublishing.org/doi/full/10.1098/rsos.231393


### Explainability of LLMs

A project to explain large-language models (LLMs) using prompt engineering based on class-contrastive counterfactuals [1,2]. This is a joint project with Prof. Pietro Lio.

This work will build on previous work. We will apply explainable AI techniques to explain black-box models such as LLMs. Techniques can include work such as the one shown below and previously published work [1]:

https://www.nature.com/articles/s41467-024-51970-x


### Building an AI powered virtual cell

This project will look at building a part of an AI powered virtual cell (AI virtual cell foundation models).

How to Build the Virtual Cell with Artificial Intelligence: Priorities and Opportunities

https://arxiv.org/pdf/2409.11654

### Open-ended play in agents

Extend the framework in the following paper:

Open-Ended Learning Leads to Generally Capable Agents

https://arxiv.org/pdf/2107.12808


### Training LLMs for computer use

https://os-world.github.io/

### Other projects

Bongard problems solve with vision models

Cellular automata using transformers



<!--
### Project idea 10 (Computational Biology)

Apply machine learning to high dimensional biological data/sequencing data. 

<!--
a Bayesian neural network

https://rdrr.io/cran/BNN/
-->

<!--
This project will look at spatial transcriptomics data.

This would be a collaboration with Dr. Tom Chittenden.
-->


<!--
### Project idea 11: Biologically inspired machine learning applied to cyber security

This project will involve developing biologically inspired machine learning techniques, like negative selection algorithms [7]. Negative selection algorithms are inspired by how the immune system is trained to detect pathogens. This project will involve developing a biologically inspired machine learning algorithm and applying it to cyber security. An example application would be detecting outliers in network traffic.
-->


<!--
### Project idea 12: AI applied to cyber security

This project will develop AI tools applied to cyber security. 

Ideas include developing and improving on AI based methods for password guessing. See PassGAN: A Deep Learning Approach for Password Guessing

https://arxiv.org/pdf/1709.00440.pdf


<!-- talk on AI applied to cyber security

https://www.youtube.com/watch?v=oBdB61A8Yt8

-->

<!--
Other ideas include extending AI based approaches to generate better phishing URLs. For example, DeepPhish: Simulating Malicious AI

https://albahnsen.files.wordpress.com/2018/05/deepphish-simulating-malicious-ai_submitted.pdf

Other ideas include designing better outlier detection algorithms in network traffic data. For example, one can use ideas from rough sets to design better outlier detection strategies:

Outlier Detection Using Rough Sets

https://link.springer.com/chapter/10.1007/978-3-030-05127-3_7

We can also use autoencoders for detecting outliers in network traffic data.

Other ideas include using deep autoencoders for detecting malicious source code

https://doi.org/10.1016/j.patter.2023.100773
-->


<!--
### Project idea 13

* Other project ideas are generating synthetic data from private datasets like data from electronic healthcare records data [3], other explanatory artificial intelligence (xAI) techniques, privacy preserving machine learning [4], documenting data and models, detecting concept drift [6], etc. 
-->

<!--
### Other ideas

 Project ideas can be developed according to student interests. If you have other project ideas you would like to discuss, please come speak with me.
 -->

<!--
### Computational virology and computational immunology

Some specific projects can involve:

* Inferring biologically relevant parameters for viral infection from time series data

Estimating biologically relevant parameters under uncertainty for experimental within-host murine West Nile virus infection, Soumya Banerjee, Jeremie Guedj, Ruy Ribeiro, Melanie Moses & Alan Perelson Journal of the Royal Society Interface, 13(117), 20160130, 2016

https://royalsocietypublishing.org/doi/full/10.1098/rsif.2016.0130

* Understanding the nature of central tolerance using publicly available genomic data

Influence of correlated antigen presentation on T cell negative selection in the thymus, Soumya Banerjee, SJ Chapman, Journal of the Royal Society Interface, 15(148), 20180311, 2018

https://royalsocietypublishing.org/doi/full/10.1098/rsif.2018.0311

-->
 
## Supervision 
 
 Students will be jointly supervised with Prof. Neil Lawrence or Prof. Pietro Lio.

## Contact

Project ideas can be developed according to student interests. 

Please contact Soumya Banerjee at sb2333@cam.ac.uk or neel.soumya@gmail.com to have an informal chat. Please also send a copy of your CV.

Office: FC01 (first floor) in the computer science department

You can learn more about my work here: 

https://sites.google.com/site/neelsoumya 

## Bigger Picture

The main objective is to develop a suite of techniques inspired by classical AI to inform explainable AI.
This project is part of a wider effort of unconventional approaches to AI. 

## References 

1. Banerjee S, Lio P, Jones PB, Cardinal RN (2021) A class-contrastive human-interpretable machine learning approach to predict mortality in severe mental illness. npj Schizophr 7: 1–13. 

2. Rudin C (2019) Stop explaining black box machine learning models for high stakes decisions and use interpretable models instead. Nat Mach Intell 1: 206–215. 

3. Banerjee S, tom rp Bishop (2022) dsSynthetic: Synthetic data generation for the DataSHIELD federated analysis system. BMC Res Notes 15: 230. 

4. Banerjee S, Sofack GN, Papakonstantinou T, Avraam D, Burton P, et al. (2022) dsSurvival: Privacy preserving survival models for federated individual patient meta-analysis in DataSHIELD. BMC Res Notes 15: 197.

5. Modelling the effects of phylogeny and body size on within-host pathogen replication and immune response, Soumya Banerjee, Alan Perelson, Melanie Moses, Journal of the Royal Society Interface 14(136), 20170479, 2017

6. https://web.archive.org/web/20230606205118/https://www.nannyml.com/blog/when-data-drift-does-not-affect-performance-machine-learning-models, URL accessed June 2023

7. Influence of correlated antigen presentation on T cell negative selection in the thymus, Soumya Banerjee, SJ Chapman, Journal of the Royal Society Interface, 15(148), 20180311, 2018



