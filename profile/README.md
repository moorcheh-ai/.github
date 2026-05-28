<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/moorcheh-ai/moorcheh-boilerplate/main/template/public/moorcheh-logo-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/moorcheh-ai/moorcheh-boilerplate/main/template/public/moorcheh-logo-light.svg">
  <img width="280px" alt="Moorcheh Logo" src="https://raw.githubusercontent.com/moorcheh-ai/moorcheh-boilerplate/main/template/public/moorcheh-logo-light.svg">
</picture>

# The World's First Information-Theoretic Search Engine

**Ultra-fast, deterministic, index-free semantic search — and the full AI infrastructure stack that grew around it.**

<p>
  <a href="https://github.com/moorcheh-ai/memanto/stargazers">
    <img src="https://img.shields.io/github/stars/moorcheh-ai/memanto?style=for-the-badge&logo=github&label=Memanto%20Stars&color=yellow" alt="Memanto Stars"/>
  </a>
</p>

<p>
  <a href="https://www.linkedin.com/company/moorcheh-ai">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=LinkedIn&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="https://x.com/moorcheh_ai">
    <img src="https://img.shields.io/badge/Follow_on_X-000000?style=for-the-badge&logo=x&logoColor=white" alt="X"/>
  </a>
  <a href="https://discord.gg/CyxRFQSQ3p">
    <img src="https://img.shields.io/badge/Join_Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Discord"/>
  </a>
  <a href="https://www.youtube.com/@moorchehai">
    <img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="YouTube"/>
  </a>
  <a href="https://www.moorcheh.ai/">
    <img src="https://img.shields.io/badge/Website-45B7D1?style=for-the-badge&logo=Google-Chrome&logoColor=white" alt="Website"/>
  </a>
</p>

</div>

---

## 🧠 What Is Moorcheh?

Moorcheh pioneered the **information-theoretic approach to semantic search** — the same foundational direction Google Research later brought to mainstream attention with their **TurboQuant** paper. We've been shipping production systems on these principles for two years, and we've gone well beyond what the academic papers describe.

While TurboQuant and RaBitQ address **compression**, Moorcheh combines three integrated components that operate as a whole:

- **MIB — Maximally Informative Binarization** · information-theoretic compression tuned to preserve *semantic* content, not just minimize geometric distortion.
- **EDM — Efficient Distance Metric** · bitwise operations on native CPU instructions, replacing the floating-point math behind cosine similarity.
- **ITS — Information-Theoretic Score** · a ranking mechanism that replaces geometric proximity as the relevance signal, with an integrated reranker. This is the part the papers don't touch — and it's why our end-to-end latency beats two-stage (search + external rerank) architectures by **~6.6×**.

> Compression alone can't get you there. Compression **plus** the right scoring function **plus** the right execution model can.

📄 **Moorcheh White Paper:** [arxiv.org/abs/2601.11557](https://arxiv.org/abs/2601.11557) · 📰 **Our take on the TurboQuant moment:** [Read the blog](https://moorcheh.ai/blog/information-theoretic-vector-search-turboquant-moment)

---

## ⚡ Proven Performance

<div align="center">

| Metric | Result | Context |
|---|---|---|
| **NDCG@10** | 64–74% | Matches float32 systems despite **32× compression** |
| **Distance Calc** | **9.6 ms** | vs 37–86 ms (PGVector, Qdrant) |
| **Throughput** | **2,000+ QPS** | Sustained, zero accuracy degradation |
| **End-to-End** | **6.6× faster** | vs Pinecone + Cohere rerank |
| **Idle Cost** | **$0** | Truly scales to zero |

</div>

Benchmarked across 14 MAIR datasets and 10,038 queries — constant throughput across all precision levels, something HNSW-based systems structurally cannot do.

---

## 🏗️ The Index-Free Architecture

Out of the engine grew a **fully serverless, cloud-native architecture** that powers large enterprise customers — saving millions while maintaining production-grade AI infrastructure and knowledge management.

Moorcheh introduced the **first index-free database architecture**: no dependence on RAM, no delay from indexing and re-indexing. It performs a **full scan of every entry in a few milliseconds** — deterministic, exact-match retrieval at any scale.

**Real impact:** one enterprise deployment went from **$2.5M/year → $36K/year** in retrieval infrastructure costs.

- ✅ **Sovereign by design** — deploys into your VPC on AWS, GCP, or Azure
- ✅ **Zero egress** — no data ever crosses your perimeter
- ✅ **True serverless economics** — scales to millions of queries or to $0 when idle
- ✅ **Deploys in under 10 minutes** via Infrastructure-as-Code

---

## 🧩 The Moorcheh Ecosystem

Everything below grew out of the core engine — a complete, open, and community-driven AI stack.

### ☁️ Moorcheh Cloud
A complete studio for testing, building, and deploying AI applications and chatbots — with **free credits**, a full playground, and a comprehensive set of functional API endpoints supporting the most complex workflows.

<p>
  <a href="https://console.moorcheh.ai/api-keys"><img src="https://img.shields.io/badge/API%20Keys-FF6B6B?style=for-the-badge&logo=key&logoColor=white" alt="API Keys"/></a>
  <a href="https://console.moorcheh.ai/playground"><img src="https://img.shields.io/badge/Playground-45B7D1?style=for-the-badge&logo=play&logoColor=white" alt="Playground"/></a>
  <a href="https://docs.moorcheh.ai"><img src="https://img.shields.io/badge/Documentation-96CEB4?style=for-the-badge&logo=book&logoColor=white" alt="Docs"/></a>
</p>

### 🐜 Memanto — Memory that AI Agents Love
A **companion memory agent** that pairs with any working agent to manage memories across sessions, tools, and time. Fully open source and community-driven, it inherits Moorcheh's deterministic retrieval — eliminating the behavioral drift that ANN-based memory introduces into multi-turn agents. Continually gaining traction with AI developers and agent builders.

<p>
  <a href="https://github.com/moorcheh-ai/memanto">
    <img src="https://img.shields.io/badge/⭐_Star_on_GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="Memanto on GitHub"/>
  </a>
  <a href="https://github.com/moorcheh-ai/memanto/stargazers">
    <img src="https://img.shields.io/github/stars/moorcheh-ai/memanto?style=flat-square&logo=github&label=Stars&color=yellow" alt="Memanto Stars"/>
  </a>
  <a href="https://pepy.tech/projects/memanto">
    <img src="https://static.pepy.tech/personalized-badge/memanto?period=total&units=international_system&left_color=grey&right_color=blue&left_text=PyPI%20Downloads" alt="Memanto PyPI Downloads"/>
  </a>
</p>

📄 **Memanto White Paper:** [arxiv.org/abs/2604.22085](https://arxiv.org/abs/2604.22085v1) · 🌐 [memanto.ai](https://memanto.ai) · 📰 [Memanto Blog](https://memanto.ai/blog) · 📈 [Download stats](https://pepy.tech/projects/memanto?timeRange=threeMonths&category=version&granularity=weekly)

### 🦅 MemantoClaw
Born from the need for higher accuracy and functionality in OpenClaw / NeMo Claw architectures. Runs **entirely through the Moorcheh API ecosystem and a single API key** — no external connectors required. The only known method of running and deploying OpenClaw bots **fully contained within an air-gapped infrastructure.**

### 🏠 Moorcheh On-Prem (Free)
A free on-premise version that pairs with **local models** and performs every cloud functionality directly from your own machine — zero cloud reliance.

### 📦 Moorcheh Edge
The newest addition: a **lightweight, containerized search engine** that runs on even the most restricted devices at incredible speed and accuracy.

### 🛠️ Open Source for Builders
Many community-driven projects help indie developers and hackers tap into Moorcheh's engine — including the **JS Chat Boilerplate**, which lets you ship a full chat application with minimal code.

---

## 🔌 Deeply Integrated Everywhere

Moorcheh plugs natively into the major AI infrastructure and agentic stacks:

<div align="center">

[![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)](https://docs.langchain.com/oss/python/integrations/vectorstores/moorcheh)
[![LlamaIndex](https://img.shields.io/badge/LlamaIndex-000000?style=for-the-badge)](https://developers.llamaindex.ai/python/examples/vector_stores/moorchehdemo/)
[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/moorcheh)
[![n8n](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io/integrations/moorcheh/)
[![MCP](https://img.shields.io/badge/MCP-000000?style=for-the-badge)](https://github.com/moorcheh-ai/moorcheh-mcp)

</div>

LangChain · LangGraph · LlamaIndex · n8n · CrewAI · Hugging Face · MCP · and more.

---

## 🚀 Quick Start

**Install the SDK:**
```bash
pip install moorcheh-sdk
```

**Build a RAG system in seconds:**
```python
import os
from moorcheh_sdk import MoorchehClient

client = MoorchehClient(api_key=os.getenv("MOORCHEH_API_KEY"))

# Create a namespace and ingest documents
client.create_namespace("my-rag", "text")
client.upload_documents("my-rag", [
    {"id": "doc1", "text": "Your content...", "metadata": {}}
])

# Get an AI-powered, grounded answer
answer = client.get_generative_answer(
    namespace="my-rag",
    query="Your question here"
)
print(answer["answer"])
```

[![PyPI Downloads](https://static.pepy.tech/personalized-badge/moorcheh-sdk?period=total&units=international_system&left_color=grey&right_color=blue&left_text=SDK%20Downloads)](https://pepy.tech/project/moorcheh-sdk)
[![Boilerplate Downloads](https://img.shields.io/npm/dt/moorcheh-chat-boilerplate?style=flat-square&label=Boilerplate)](https://www.npmjs.com/package/moorcheh-chat-boilerplate)
[![n8n Downloads](https://img.shields.io/npm/dt/n8n-nodes-moorcheh?style=flat-square&label=n8n%20Nodes)](https://www.npmjs.com/package/n8n-nodes-moorcheh)

---

## 📚 Featured Repositories

| Repo | ⭐ Stars | Description |
|---|---|---|
| [**memanto**](https://github.com/moorcheh-ai/memanto) | ![](https://img.shields.io/github/stars/moorcheh-ai/memanto?style=flat-square&label=&color=yellow) | 🐜 Memory that AI Agents Love — the companion memory agent |
| [**moorcheh-python-sdk**](https://github.com/moorcheh-ai/moorcheh-python-sdk) | ![](https://img.shields.io/github/stars/moorcheh-ai/moorcheh-python-sdk?style=flat-square&label=&color=yellow) | 🐍 Official Python SDK for the Moorcheh Semantic Search API |
| [**moorcheh-chat-boilerplate**](https://github.com/moorcheh-ai/moorcheh-chat-boilerplate) | ![](https://img.shields.io/github/stars/moorcheh-ai/moorcheh-chat-boilerplate?style=flat-square&label=&color=yellow) | 💬 Production-ready Next.js chat app powered by ITS search + RAG |
| [**moorcheh-mcp**](https://github.com/moorcheh-ai/moorcheh-mcp) | ![](https://img.shields.io/github/stars/moorcheh-ai/moorcheh-mcp?style=flat-square&label=&color=yellow) | 🔌 MCP server bringing Moorcheh search & RAG to MCP clients |
| [**memantoclaw**](https://github.com/moorcheh-ai/memantoclaw) | ![](https://img.shields.io/github/stars/moorcheh-ai/memantoclaw?style=flat-square&label=&color=yellow) | 🦅 Air-gapped OpenClaw deployment via the Moorcheh API |
| [**langchain-moorcheh**](https://github.com/moorcheh-ai/langchain-moorcheh) | ![](https://img.shields.io/github/stars/moorcheh-ai/langchain-moorcheh?style=flat-square&label=&color=yellow) | 🦜 Seamless LangChain ↔ Moorcheh integration |
| [**n8n-nodes-moorcheh**](https://github.com/moorcheh-ai/n8n-nodes-moorcheh) | ![](https://img.shields.io/github/stars/moorcheh-ai/n8n-nodes-moorcheh?style=flat-square&label=&color=yellow) | ⚡ n8n nodes for ingestion, semantic search & AI workflows |
| [**moorcheh-examples**](https://github.com/moorcheh-ai/moorcheh-examples) | ![](https://img.shields.io/github/stars/moorcheh-ai/moorcheh-examples?style=flat-square&label=&color=yellow) | 📓 Practical sample projects and integration recipes |
| [**moorcheh-benchmarks**](https://github.com/moorcheh-ai/moorcheh-benchmarks) | ![](https://img.shields.io/github/stars/moorcheh-ai/moorcheh-benchmarks?style=flat-square&label=&color=yellow) | 📊 Benchmarks, experiments, and use cases |

➡️ **[Browse all repositories →](https://github.com/orgs/moorcheh-ai/repositories)**

---

## 💡 Use Cases

Real, runnable examples across regulated and document-heavy domains:

| | |
|---|---|
| [📂 Analyzing Codebases](https://github.com/moorcheh-ai/moorcheh-examples/tree/main/AnalyzingCodebases_WithFirecrawlAndLlamaIndex) | Moorcheh + Firecrawl + LlamaIndex |
| [💰 Financial Documents](https://github.com/moorcheh-ai/moorcheh-examples/tree/main/AnalyzingFinancialDocuments_WithLangChain) | Moorcheh + LangChain |
| [🌍 Geographical Documents](https://github.com/moorcheh-ai/moorcheh-examples/tree/main/AnalyzingGeographicalDocuments_WithLlamaIndex) | Moorcheh + LlamaIndex |
| [🏥 Healthcare Documents](https://github.com/moorcheh-ai/moorcheh-examples/tree/main/AnalyzingHealthcareDocuments_WithLlamaIndex) | Moorcheh + LlamaIndex |
| [⚖️ Legal Documents](https://github.com/moorcheh-ai/moorcheh-examples/tree/main/AnalyzingLegalDocuments_WithLlamaIndex) | Moorcheh + LlamaIndex |
| [🔬 Scientific Journals](https://github.com/moorcheh-ai/moorcheh-examples/tree/main/AnalyzingScientificJournals_WithLangChain) | Moorcheh + LangChain |

---

## 📖 Learn More

- 🌐 **Website:** [moorcheh.ai](https://moorcheh.ai)
- 📝 **Moorcheh Blog:** [moorcheh.ai/blog](https://moorcheh.ai/blog)
- 🐜 **Memanto:** [memanto.ai](https://memanto.ai) · [memanto.ai/blog](https://memanto.ai/blog)
- 📄 **Moorcheh Paper:** [arxiv.org/abs/2601.11557](https://arxiv.org/abs/2601.11557)
- 📄 **Memanto Paper:** [arxiv.org/abs/2604.22085](https://arxiv.org/abs/2604.22085v1)
- 📚 **Docs:** [docs.moorcheh.ai](https://docs.moorcheh.ai)

---

<div align="center">

### Transform your search. Elevate your AI.

**Built for developers, trusted by enterprises.**

🇨🇦 Made with ❤️ by [Edge AI Innovations Inc.](https://www.moorcheh.ai/)

</div>
