# Hi, I'm Kyle Coletta 👋

**MS in Data Science @ Columbia University** (expected December 2026, 4.00 GPA) · New York, NY

I build LLM agents and the systems that keep them honest: natural-language interfaces to data, deterministic guardrails and evaluation for agents, and fine-tuned small models. Everything below is deployed or in a public repo, not left in a notebook.

Before Columbia I spent four years at Princeton Consultants leading a team of 10+ developers and QA on a multi-year, multimillion-dollar modernization for a Fortune 500 client. Now I research coding-agent safety at Columbia's Data, Agents, and Processes Lab (DAPLab) and ship LLM applications end to end, from data pipeline to fine-tuning to deployment.

**Open to full-time ML / AI engineering roles starting early 2027.** US citizen, based in New York, remote-friendly.

[![Website](https://img.shields.io/badge/Website-kylecoletta.com-222222?style=flat&logo=googlechrome&logoColor=white)](https://kylecoletta.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-kylecoletta-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kylecoletta)
[![Email](https://img.shields.io/badge/Email-kc3936%40columbia.edu-B31B1B?style=flat&logo=gmail&logoColor=white)](mailto:kc3936@columbia.edu)

---

## At a glance

- **Agents in production:** [StatIt](https://www.stat-it.com), a public NFL stats engine with self-correcting text-to-SQL and a multi-step tool-use agent, built and run solo since early 2026
- **Agent safety research:** Data Flow Control at Columbia DAPLab, a policy layer that deterministically stops coding agents from breaking user-defined rules
- **First place**, AWS x AGI House Small Language Model Hackathon (November 2025), with a LoRA fine-tuned TinyLlama shipped as a Chrome extension
- **Four years** turning ambiguous business requirements into delivered software for a Fortune 500 client, presenting to product owners and executives along the way

---

## What I'm working on now

### Data Flow Control · Columbia DAPLab (June 2026 to present)
A policy-enforcement framework inside LLM harnesses that deterministically blocks tool calls and shell commands violating user-defined data-flow rules. I built the Python pipeline that parses and classifies 80,000+ shell commands (2,100+ distinct) from SWE-bench Pro agent trajectories against a canonical taxonomy, raising functional coverage from 85% to 99.8%, and I set up the AWS Bedrock inference profiles and Docker containers for the benchmark that measures the framework's effect on resolve rate, with baseline and restricted runs across two agent harnesses. Result so far: zero resolve-rate regression under the restricted policy.

### Next-Edit Prediction for Code Completion · MS capstone sponsored by IBM (Fall 2026)
A five-person team extending Zed's open-source [Zeta](https://github.com/zed-industries/zeta) edit-prediction work: growing the dataset, building evaluations, and training models with LoRA supervised fine-tuning and DPO. Deliverables are a model, a report, and a paper.

### Lou · NYC scavenger-hunt agent ([repo](https://github.com/jan-barg/scavagent), [live](https://scavagent-b57mvtutma-ue.a.run.app))
Built with Jan Barganowski for Columbia's Agentic AI course in one week this October. Tell Lou where you are and how long you have, and it researches real places from Wikipedia and NYC landmark records, times the route with live transit data, writes a mystery with a clue earned at each stop, and guides you one stop at a time. My half: the deterministic plan evaluator (50+ violation codes, each returned with a fix the model applies itself), the agent instructions, the Wikipedia and NYC Landmarks research tools, and the transit routing. 341 Python tests.
`FastAPI` `LiteLLM` `Claude Sonnet` `Google Cloud Run`

---

## Projects

### [StatIt](https://github.com/colettak16/StatIt) · natural-language NFL stats engine · [stat-it.com](https://www.stat-it.com)
Ask a question in plain English, get an answer with charts, over a custom 1999-to-present stats database. Validated, self-correcting text-to-SQL (SELECT-only validator, read-only database role, failed queries retried with the Postgres error fed back), plus an agent mode where a multi-step tool-use agent plans an analysis, runs SQL, builds charts, and streams a written synthesis over SSE. Supabase auth, per-user quotas and rate limiting that bound API cost, query history, and a weekly GitHub Actions sync from nflverse that fails loudly on schema drift. Built solo and used by the public.
`React` `FastAPI` `PostgreSQL` `Claude API` `Supabase` `Railway` `Vercel`

### Promptly · AWS x AGI House Small Language Model Hackathon, first place (November 2025) · [repo](https://github.com/HenriqueSchmitz/small-language-model-hackathon)
Inline Chrome extension that reads what you type into an LLM chatbot and suggests ways to make the prompt more effective, powered by a LoRA fine-tuned TinyLlama trained on AWS Trainium. Idea to working demo in one weekend with my team.
`TinyLlama` `LoRA` `AWS Trainium` `Chrome Extension`

### [Aura](https://github.com/colettak16/aura-therapy-chat) · CBT-informed therapy chatbot · [live demo](https://aura-therapy-chat.onrender.com/)
Free, publicly accessible chatbot from an Applied Machine Learning team project. Llama 3.2 fine-tuned with LoRA on paired preferred and rejected therapist responses, served from a Hugging Face inference endpoint behind a web app on Render, with a dual-model fallback (currently running the fallback model to keep hosting free).
`Llama 3.2` `LoRA` `PyTorch` `Hugging Face` `Render`

### [Personal portfolio with ColettaBot](https://github.com/colettak16/coletta_website) · [kylecoletta.com](https://kylecoletta.com)
Portfolio site with a RAG chatbot that answers questions about my background and projects, grounded in chunked documents and served from Vercel serverless functions.
`Claude API` `OpenAI Embeddings` `Supabase pgvector` `Vercel`

### [AWS x NFL Big Data Bowl](https://github.com/colettak16/AWSxNFL-Big-Data-Bowl) · [report](https://colettak16.github.io/AWSxNFL-Big-Data-Bowl/)
Co-authored analysis of 2023-season NFL play and player-tracking data, entered in the Kaggle competition's University Track and published as a Quarto site. Ranked offensive formations against defensive coverages by EPA, and showed that play action increases receiver separation on nearly every route type.
`R` `ggplot2` `Quarto`

---

## Experience

**Columbia DAPLab** · MS Graduate Researcher · June 2026 to present
Coding-agent safety and evaluation research (Data Flow Control, above).

**Princeton Consultants** · Associate I to Senior Associate II · February 2021 to May 2025
Managed 10+ developers and QA on a multi-year Fortune 500 software modernization under an Agile workflow. Owned timelines, implementation strategy, and budget for a multimillion-dollar project, and presented progress and risks to product owners and executives, including a mid-project re-scope that the client approved as an expanded Statement of Work. Reverse-engineered a poorly documented legacy system by interviewing subject matter experts, reading COBOL source, and validating behavior with Python and SQL.

**Earlier:** QA and test automation intern at DISH Network (Python scripts parsing test artifacts into a standardized format); business intern at the U.S. Securities and Exchange Commission (explained an ML model's abnormal-trading flags with ggplot2 visualizations for a non-technical audience).

---

## How I work

- I build with AI coding agents every day, Claude Code most of all, and I keep a critical eye on what they produce: my research is literally about catching what coding agents get wrong.
- I automate the tedious parts of my own life. The latest is a small script that checks Luma twice a week and has an LLM pick out the networking events worth my time.
- I like owning a problem end to end, and I communicate early: blockers get raised the day they appear, not the week after.

---

## Tech stack

**Languages:** Python · SQL · R
**ML & LLMs:** PyTorch · scikit-learn · Hugging Face · LoRA fine-tuning · RAG · Claude API · OpenAI API · agent evaluation (SWE-bench Pro) · Pandas · NumPy
**Backend & data:** FastAPI · PostgreSQL · Supabase (Auth, pgvector) · React · GitHub Actions
**Cloud & tools:** Docker · AWS Bedrock · Railway · Vercel · Render · Git · Claude Code · Jira · Figma · Postman · Splunk
**Visualization:** ggplot2 · Quarto · Chart.js

---

## Education

**Columbia University** · MS in Data Science · expected December 2026 · GPA 4.00/4.00
Coursework: Machine Learning, Deep Learning, Agentic AI, NLP, Probability, Statistical Inference, Data Analysis and Visualization, Algorithms

**University of Michigan** · BS in Computer Science, Minor in Applied Statistics · 2020
Michigan Sports Analytics Society: fantasy lineup optimization and the society's annual hackathons

---

Interests, in and out of code: LLM agents and agent safety, text-to-SQL and natural-language interfaces to data, efficient small models, and sports analytics (NFL first, then everything else).
