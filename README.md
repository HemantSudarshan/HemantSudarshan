# Hemant Sudarshan

**Applied AI Engineer at Dhumi · Bengaluru, India**

I build end-to-end web applications and integrate AI into the workflows they support. My work spans web data collection, model fine-tuning and serving, retrieval and agents, backend APIs, and deployment on Azure and AWS. I use AI to iterate quickly and apply engineering judgment to what I automate, test, and ship.

[Portfolio](https://hemantsudarshan.vercel.app/) · [LinkedIn](https://www.linkedin.com/in/hemant-sudarshan-01633928a/) · [Kaggle](https://www.kaggle.com/hemantsudarshan) · [Hugging Face](https://huggingface.co/Hemantxai)

[Request my résumé](mailto:collabwithhemantgenai@gmail.com?subject=Resume%20request)

**Top skills** · Microsoft Foundry (Azure AI Foundry) · Context engineering · LLM fine-tuning · Reverse engineering · MERN stack · Amazon Bedrock

## Experience

### End-to-end AI engineering at Dhumi

**Applied AI Engineer · Mar 2026–present**

#### Workflow and application design

I start by mapping where users spend time gathering information, repeating decisions, or moving data between systems. That helps me decide what data the application needs, where a model or agent can help, what should happen in the backend, and which outcomes to test before deployment.

#### Bright Data scrapers and web data pipelines

I build **Bright Data scrapers** for web data collection and custom datasets. My work includes proxy handling, extracting structured records from web pages, and using Azure Functions for automation. I connect collected data to downstream AI workflows and the business applications that use it.

I presented a Dhumi demo on turning marketplace listings into structured data for price monitoring, competitor research, and market analysis. [Dhumi on LinkedIn](https://in.linkedin.com/company/dhumi)

#### Open-weight model fine-tuning and serving

I experiment with Qwen and Gemma checkpoints, use Unsloth for fine-tuning, and host models through Microsoft Foundry. I work through the path from preparing a dataset and adapting a model to exposing it as an endpoint that an agent or application can call.

#### Retrieval, context engineering, and agents

I build retrieval-augmented generation (RAG), conversational AI, and workflows that coordinate multiple agents. I use Microsoft Foundry, Foundry Agent Service, and Microsoft Agent Framework for agent development. For each step, I design the system instructions, retrieved passages, tool inputs, and conversation state the model needs. I tune that context with response quality, latency, and token use in mind.

#### Full-stack development and business integrations

I build full-stack web applications and the REST APIs that connect AI features to CRMs, ERPs, and other services. I manage databases and configure service identities, authentication, authorization, and permissions so backends can access data and cloud resources securely. I add vector search for retrieval and use queues and background workers for longer-running jobs. My backend work spans Python and FastAPI, along with Node.js and Express.js.

#### Azure delivery and operations

I deploy and manage complete application stacks on Azure, including containerized services. I test workflow edge cases and use logs and monitoring to track how the system behaves after deployment. I also contribute reusable agent skills, engineering planning guides, and standardized prompt packs to Dhumi’s public AI resource library.

### Earlier experience

#### Pratilipi · AI Operations & Localization Consultant

**Aug 2025–Mar 2026**

Supported AI-assisted localization and multilingual content operations in Hindi, Telugu, and Kannada. I applied generative AI tools to the translation and content-processing steps that the localization team repeated across languages.

#### Pratilipi · Localization Operations & Gen AI Intern

**Feb–Aug 2025**

Built LLM-assisted translation utilities and automated repetitive content-processing tasks for multilingual localization.

#### AppiVa Software Pvt Ltd · Machine Learning Intern

**Aug–Nov 2023**

Worked on data preprocessing, analytics, and machine learning model development.

## Open-source contributions

**12 merged pull requests across seven upstream projects**, including six in OpenClaw. My contributions cover browser automation, gateway recovery, document parsing, persistence, and data tooling.

### OpenClaw

- **Remote browser automation.** Added timeouts to remote tab enumeration over Playwright and Chrome DevTools Protocol. Fixed the default user browser profile so it honors the configured CDP endpoint. [#80147](https://github.com/openclaw/openclaw/pull/80147) · [#80143](https://github.com/openclaw/openclaw/pull/80143)
- **Gateway recovery.** Resolved session-lock conflicts when a gateway timeout triggered an embedded fallback. Handled transient Telegram network errors that could terminate the gateway. [#74543](https://github.com/openclaw/openclaw/pull/74543) · [#74549](https://github.com/openclaw/openclaw/pull/74549)
- **Messages and model status.** Fixed duplicate assistant media replies in the Control UI and corrected context-window reporting when a channel overrides the model. [#75481](https://github.com/openclaw/openclaw/pull/75481) · [#74534](https://github.com/openclaw/openclaw/pull/74534)

### Other upstream projects

- **Lance.** Added edit-distance suggestions for missing schema fields in Rust. The suggestions are computed when the error is displayed and use an inline implementation. [#5976](https://github.com/lance-format/lance/pull/5976)
- **VectorLiteDB.** Implemented crash-safe saves using a temporary file and atomic replacement to protect the database during interrupted writes. [#3](https://github.com/vectorlitedb/vectorlitedb/pull/3)
- **Docling.** Fixed DOCX parsing for hyperlinks with missing target addresses. [#3022](https://github.com/docling-project/docling/pull/3022)
- **Keploy.** Replaced the legacy zero-key map pattern for proxy sessions and mock managers with synchronized direct references in Go. [#3895](https://github.com/keploy/keploy/pull/3895)
- **FiftyOne.** Fixed frame-label retrieval by re-fetching labels after cache misses on long videos. [#7053](https://github.com/voxel51/fiftyone/pull/7053)
- **Xberg (formerly Kreuzberg).** Fixed migration guide regressions and refreshed Python demos. [#389](https://github.com/xberg-io/xberg/pull/389)

[Browse merged pull requests](https://github.com/pulls?q=is%3Apr+is%3Amerged+author%3AHemantSudarshan)

## Technical toolkit

I’ve deployed AI agents through Amazon Bedrock.

| Area | Tools and technologies |
| --- | --- |
| Model training and serving | PyTorch, Unsloth, Qwen, Gemma, Microsoft Foundry |
| Agent and retrieval systems | Microsoft Agent Framework, Foundry Agent Service, LangGraph |
| Frontend | React, TypeScript, Tailwind CSS, Vite |
| Backend | Node.js, Express.js, Python, FastAPI, REST APIs |
| Data and retrieval | MongoDB, PostgreSQL, Redis, Weaviate, Qdrant |
| Web data collection | Bright Data, Firecrawl, proxy handling |
| Containers | Docker, Docker Compose |
| Azure deployment | Azure container deployments, Azure Functions |
| AWS deployment | Amazon ECR for container images, Amazon EC2 and Amazon Lightsail for application hosting, AWS Amplify for frontend deployments |
| Upstream contributions | Rust, Go |

## Selected projects

### Small Language Model from Scratch · Attention Study

I trained a tokenizer and a six-layer Transformer from scratch on TinyStories. I compared multi-head attention (MHA), grouped-query attention (GQA), multi-query attention (MQA), and multi-head latent attention (MLA) to study how attention choices affect validation loss, key-value (KV) cache size, and decoding.

- **Experimental setup.** About 13–15 million parameters across configurations, 20 primary training runs across five seeds, and four parameter-matched controls. Each primary run processed about 283 million tokens on a Tesla T4.
- **Quality and stored cache.** MHA reached the lowest mean validation loss at 1.5244 nats. GQA with four KV heads used one-third of MHA’s stored KV-cache memory, with an observed mean loss increase of 0.0076 nats. The five-seed paired comparison returned a p-value of 0.125.
- **Decoding on the T4.** In the backend I tested, the compact GQA operation took 2.69× as long as the implementation that explicitly repeated the key and value heads. My measurements cover both stored cache bytes and actual decoding time.
- **Cached decoding.** I checked cached outputs against full-sequence attention and tested position-aware causal masking for cases where decoding adds multiple tokens at once.

[Read the experiment and notebook](https://www.kaggle.com/code/hemantsudarshan/small-language-model-from-scratch-attention-study)

### College projects

#### Agentic Inventory Restocking Service

An inventory workflow for deciding when and how to replenish stock. It loads sales and stock data, calculates safety stock and reorder points from demand variability and lead time, then passes those figures to the recommendation step. LangGraph coordinates the data loading, calculation, reasoning, and action generation. The action is recorded as a purchase or transfer order, with lower-confidence recommendations routed to Telegram for human approval. The project includes a FastAPI service and MongoDB persistence.

[Inventory repository](https://github.com/HemantSudarshan/Agentic-Inventory-Restocking-Servic) · [LangGraph workflow](https://github.com/HemantSudarshan/Agentic-Inventory-Restocking-Servic/blob/main/workflow/graph.py) · [Safety-stock calculations](https://github.com/HemantSudarshan/Agentic-Inventory-Restocking-Servic/blob/main/agents/safety_calculator.py)

#### Compliance-GPT

A RAG application for asking questions about regulatory documents and tracing answers back to the passages that support them. The ingestion pipeline preserves page references and document metadata as it chunks PDFs. The Weaviate retriever combines BM25 keyword search with semantic similarity and exposes the weighting. A Groq-backed generator produces answers with citations, and a verification step checks citations against retrieved text and records confidence. The evaluation module tracks faithfulness, answer relevance, and context precision.

[Compliance-GPT repository](https://github.com/HemantSudarshan/Compliance-GPT) · [Hybrid retrieval](https://github.com/HemantSudarshan/Compliance-GPT/blob/main/src/storage/retriever.py) · [Citation verification](https://github.com/HemantSudarshan/Compliance-GPT/blob/main/src/generation/citation_verifier.py)

#### AudioRAG Enterprise

A retrieval pipeline for searching and asking questions about multi-speaker recordings. AssemblyAI transcribes the audio and labels speakers. The pipeline embeds transcript text with BGE via LlamaIndex, indexes it in Qdrant, and uses SambaNova for conversational answers. Docker Compose brings together the application services, Qdrant, Redis, and PostgreSQL. The repository also includes batch workers and a FastAPI interface.

[AudioRAG repository](https://github.com/HemantSudarshan/AudioRaG_FTSambanova) · [Retrieval pipeline](https://github.com/HemantSudarshan/AudioRaG_FTSambanova/blob/main/rag_code.py) · [Docker Compose setup](https://github.com/HemantSudarshan/AudioRaG_FTSambanova/blob/main/docker-compose.yml)

## What I’m actively exploring

I see **on-premises AI infrastructure** as a major part of the next phase of AI engineering. I’m actively building the skills to deploy and operate models on infrastructure that organizations control.

- **Small language models and inference engineering.** Fine-tuning smaller open-weight models and studying how serving choices affect quality, latency, throughput, and memory.
- **Computational drug discovery.** Researching how to build drug discovery pipelines using open datasets.
- **Quantum computing.** Learning the fundamentals with a practical focus.

## Education, research, and recognition

- **Dayananda Sagar University.** B.Tech in Computer Science Technology, First Class, 2021–2025. Served as a department student representative and coordinator.
- **VibeCon 2026.** Top 20 finalist with my team at Emergent’s India event. [Team recap](https://www.linkedin.com/posts/sourish-pachiyappan_vibecon-2026-has-been-one-of-those-rare-experiences-activity-7451141632101642240-HQel)
- **Journal article.** Co-authored *Survey of AI-Driven Platforms for Welfare and Emergency Services: Gaps, Architectures and the Case for Unified Systems*, GRENZE International Journal of Engineering and Technology, Vol. 11, Issue 2, pp. 9911–9916, 2025. [Publisher’s article page](https://thegrenze.com/abstract/journal/5567)
- **Conference presentation.** *Discovering Insights into Heart Health: A Survey of Data Mining and Machine Learning Methods*, ICCICCT 2023.
- **Patent application.** Co-inventor on Indian application **202341040746** for multi-factor security in IoT devices, filed in June 2023. [Patent Office Journal entry](https://gmrit.edu.in/PDFs/Patents/2023-28.pdf)

## Contact

I’m open to freelance applied AI and full-stack projects. I’m interested in work that connects data collection, models, and agents to a workflow a team uses. [Email me](mailto:collabwithhemantgenai@gmail.com)
