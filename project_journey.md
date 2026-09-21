# AI-Powered Investor Intelligence Platform

> End-to-end Financial Document Intelligence Platform using Azure OpenAI, Azure AI Search, PostgreSQL, FastAPI, HTML/CSS and AKS.

---

## Project Goal

Build an enterprise-grade application capable of:

* Processing financial reports
* Extracting key financial insights
* Generating analytics dashboards
* Supporting RAG-based financial research
* Deploying to Azure Kubernetes Service (AKS)

---

## Phase 1: Project Planning

**Status:** Completed

### Activities

- Selected financial statement analysis as the primary use case.
- Chose annual reports as the primary data source.
- Selected Tesla, Apple and Microsoft annual reports.
- Defined the overall document intelligence and retrieval approach.
- Decided to build an investor intelligence platform rather than a standalone chatbot.
- Defined the initial dashboard and financial research direction.

---

## Phase 2: Dataset Preparation

**Status:** Completed

### Activities

- Collected publicly available annual reports.
- Prepared annual report PDFs for processing.
- Organized source documents under:

```text
data/raw_pdfs/
```

### Companies

- Apple
- Microsoft
- Tesla

---

## Phase 3: PDF to Markdown Conversion

**Status:** Completed

### Module

```text
ingestion/pdf_to_markdown.py
```

### Objective

Convert financial report PDFs into structured markdown suitable for downstream document processing and AI workflows.

### Library

```text
PyMuPDF4LLM
```

### Output

```text
data/markdown/
```

The converted reports provide the document representation used by subsequent processing stages.

---

## Phase 4: Semantic Document Chunking

**Status:** Completed

### Module

```text
ingestion/semantic_chunker.py
```

### Objective

Split financial documents into semantically meaningful chunks for downstream retrieval.

### Technology

```text
LangChain SemanticChunker
```

### Embeddings

Azure OpenAI embeddings are used as part of the semantic processing workflow.

### Output

Semantic document chunks prepared for search and retrieval.

---

## Phase 5: Project Configuration

**Status:** Completed

### File

```text
config/settings.yaml
```

### Objective

Establish centralized project configuration for application and Azure service settings.

### Configuration Areas

- Frontend configuration
- Azure AI Search configuration
- Azure OpenAI configuration
- Backend service configuration

This phase establishes the configuration foundation used by subsequent integrations.

---

## Phase 6: Azure OpenAI Integration

**Status:** Completed

### Module

```text
llm/azure_openai.py
```

### Objective

Centralize Azure OpenAI client and model configuration for the platform.

### Responsibilities

- Azure OpenAI endpoint configuration
- API configuration
- Embedding model initialization
- GPT model configuration
- Shared Azure OpenAI client functionality

---

## Phase 7: Azure AI Search Integration

**Status:** Completed

### Modules

```text
vectorstore/azure_ai_search.py
vectorstore/create_index.py
rag/retrieval_debug.py
```

### Objective

Create the searchable vector store used for financial document retrieval.

### Responsibilities

- Create Azure AI Search indexes
- Upload document chunks
- Store searchable document content
- Perform search and retrieval
- Support metadata-based filtering
- Provide retrieval debugging utilities

### Output

A searchable Azure AI Search index containing processed financial document content.

---

## Phase 8: RAG-Based KPI Extraction

**Status:** Completed

### Modules

```text
rag/kpi_extractor_rag.py
rag/__init__.py
```

### Objective

Use retrieved financial document context to extract structured financial information from annual reports.

### Financial Metrics

- Revenue
- Net Income
- Operating Income
- Cash Flow
- Total Assets
- Total Liabilities
- Risk Factors
- Growth Drivers

### Output

```text
Structured Financial Metrics
```

The extracted metrics are prepared for persistence and later application consumption.

---

## Phase 9: PostgreSQL Metrics Integration

**Status:** Completed

### Modules

```text
database/
├── __init__.py
├── create_table.py
├── metrics.py
├── postgres_sql.py
└── save_metrics.py
```

### Objective

Persist extracted financial metrics in PostgreSQL for application and dashboard consumption.

### Responsibilities

- Establish PostgreSQL connections
- Create the target database when required
- Create the `financial_metrics` table
- Save extracted financial metrics
- Retrieve stored financial metrics

### Database

```text
PostgreSQL
```

The database layer provides persistent storage between the extraction pipeline and the application layer.

---

## Phase 10: FastAPI Backend

**Status:** Pending

### Files

```text
app.py
main.py
routes/
├── __init__.py
├── chat.py
├── dashboard.py
├── health.py
└── ingestion.py
```

### Objective

Build the application backend that connects document processing, retrieval, financial metrics and the user interface.

### Planned Responsibilities

- Document ingestion
- Dashboard data
- Financial metrics access
- AI research/chat functionality
- Health checks
- Application routing

---

## Phase 11: Investor Dashboard

**Status:** Pending

### Files

```text
templates/dashboard.html
static/style.css
```

### Objective

Provide a browser-based investor dashboard for viewing financial metrics and interacting with the platform.

### Planned Capabilities

- Financial KPI visualization
- Company-level financial information
- Investor-oriented analytics
- AI Analyst interaction
- Document ingestion interface
- Financial research workflow

### Frontend Approach

```text
HTML/CSS
FastAPI + Jinja templates
```

The platform does not use React as its application frontend.

---

## Phase 12: Containerization

**Status:** Pending

### File

```text
dockerfile
```

### Objective

Package the application into a container suitable for deployment.

### Planned Deliverables

- Application Docker image
- Containerized FastAPI application
- Deployment-ready runtime configuration

---

## Phase 13: Kubernetes / AKS Deployment

**Status:** Pending

### Files

```text
k8s/
├── deployment.yaml
└── service.yaml
```

### Objective

Deploy the containerized InvestorLens application to Azure Kubernetes Service.

### Planned Components

- Kubernetes deployment
- Kubernetes service
- Azure Container Registry integration
- Azure Kubernetes Service deployment
- Application configuration and secrets

---

## Phase 14: CI/CD Automation

**Status:** Pending

### File

```text
.github/workflows/deploy.yaml
```

### Supporting Documentation

```text
CICD_Deployment_Guide.md
deployment-Document.md
```

### Objective

Automate the build and deployment workflow for the application.

### Planned Workflow

```text
GitHub
   ↓
GitHub Actions
   ↓
Docker Build
   ↓
Azure Container Registry
   ↓
Azure Kubernetes Service
```

### Responsibilities

- Authenticate with Azure
- Build the application container
- Push the image to Azure Container Registry
- Configure AKS credentials
- Apply Kubernetes manifests
- Restart and validate the deployment

---

## Development Progress

Current development state:

```text
Phase 1   Project Planning                 ✓
Phase 2   Dataset Preparation              ✓
Phase 3   PDF to Markdown Conversion       ✓
Phase 4   Semantic Document Chunking       ✓
Phase 5   Project Configuration            ✓
Phase 6   Azure OpenAI Integration         ✓
Phase 7   Azure AI Search Integration      ✓
Phase 8   RAG-Based KPI Extraction        ✓
Phase 9   PostgreSQL Integration           ✓
Phase 10  FastAPI Backend                  → next
Phase 11  Investor Dashboard               ○
Phase 12  Containerization                 ○
Phase 13  Kubernetes / AKS Deployment      ○
Phase 14  CI/CD Automation                 ○
```
---

## Final Deliverable

AI-Powered Investor Intelligence Platform

Capabilities:

* Financial Report Processing
* Semantic Search
* KPI Extraction
* Dashboard Analytics
* Company Comparison
* RAG-Based Financial Research
* Cloud-Native Deployment