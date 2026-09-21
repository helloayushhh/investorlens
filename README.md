<p align="center">
  <img src="docs/assets/investorlens-banner.png" alt="InvestorLens Banner" width="850" />
</p>

<p align="center">
  <strong>An AI-powered investor intelligence platform for financial research and analysis.</strong>
</p>

<p align="center">
  <a href="https://www.python.org/"><img alt="Python" src="https://img.shields.io/badge/python-3.12-3776AB?logo=python&logoColor=white" /></a>
  <a href="https://azure.microsoft.com/en-us/products/ai-services/openai-service"><img alt="Azure OpenAI" src="https://img.shields.io/badge/ai-azure%20openai-0078D4?logo=microsoftazure&logoColor=white" /></a>
  <a href="https://azure.microsoft.com/en-us/products/ai-services/ai-search"><img alt="Azure AI Search" src="https://img.shields.io/badge/search-azure%20ai%20search-0078D4?logo=microsoftazure&logoColor=white" /></a>
  <a href="https://docs.astral.sh/uv/"><img alt="UV" src="https://img.shields.io/badge/package%20manager-uv-6E56CF" /></a>
</p>

<p align="center">
  <a href="#overview">overview</a> ·
  <a href="#progress">progress</a> ·
  <a href="#technology">technology</a> ·
  <a href="#project-structure">project structure</a> ·
  <a href="#documentation">documentation</a> ·
  <a href="#roadmap">roadmap</a>
</p>

---

<h2 align="center">overview</h2>

**InvestorLens** is an AI-powered investor intelligence platform being developed to simplify financial research and analysis.

The project uses annual reports as its primary data source and explores how document processing, semantic search, and AI can turn financial reports into searchable knowledge and structured insights.

---

<h2 align="center">progress</h2>

**🚧 active development · phase 5 / 14**

**current phase:** project configuration

The detailed implementation progress is maintained in [`project_journey.md`](project_journey.md).

---

<h2 align="center">technology</h2>

| Layer | Technology |
| --------------------- | ---------------------------- |
| **Language** | Python 3.12 |
| **Document processing** | PyMuPDF4LLM |
| **Semantic chunking** | LangChain SemanticChunker |
| **AI & embeddings** | Azure OpenAI |
| **Search & retrieval** | Azure AI Search |
| **Package management** | UV |

---

<h2 align="center">project structure</h2>

```text
investorlens/
├── docs/
│   ├── assets/
│   │   └── investorlens-banner.png
│   ├── Business Requirements.docx
│   ├── InvestorLens_PRD.docx
│   ├── InvestorLens_TRD.docx
│   ├── Logical Arch & Notes.excalidraw
│   ├── Physical-architecture.drawio
│   └── Presentation.pptx
│
├── config/
│   └── settings.yaml
│
├── ingestion/
│   ├── __init__.py
│   ├── ingest_documents.py
│   ├── pdf_to_markdown.py
│   └── semantic_chunker.py
│
├── llm/
│   ├── __init__.py
│   └── azure_openai.py
│
├── vectorstore/
│   ├── __init__.py
│   ├── azure_ai_search.py
│   └── create_index.py
│
├── .dockerignore
├── .gitignore
├── project_journey.md
├── README.md
└── requirements.txt
```

---

<h2 align="center">documentation</h2>

- **BRD** — business requirements and project scope
- **PRD** — product requirements and user flows
- **TRD** — technical requirements and implementation direction
- **Architecture diagrams** — logical and physical architecture
- **Project Journey** — phase-by-phase development progress
- **Presentation** — project overview

Detailed documentation is available in `docs/` and `project_journey.md`.

---

<h2 align="center">roadmap</h2>

The platform is being developed across 14 phases:

1.  project planning
2.  dataset preparation
3.  PDF to markdown conversion
4.  semantic chunking
5.  project configuration
6.  Azure OpenAI integration
7.  Azure AI Search integration
8.  KPI extraction and RAG
9.  PostgreSQL metrics integration
10. FastAPI backend
11. investor dashboard
12. containerization
13. AKS deployment
14. CI/CD automation

---

See you in the next phase.

**— aps**

