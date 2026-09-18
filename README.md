# investorlens

an ai-powered investor intelligence platform for financial document research and analysis.

## project status

🚧 active development

**current phase:** phase 6 — azure ai search integration

## about

investorlens explores how ai, semantic search, and financial documents can be combined to make investment research more structured and accessible.

the current implementation focuses on building the document ingestion and retrieval foundation.

## current capabilities

* annual report processing
* pdf to markdown conversion
* semantic document chunking
* azure openai embeddings
* azure ai search
* vector search
* metadata filtering

## technology stack

* **python 3.12**
* **fastapi** *(planned)*
* **azure openai**
* **azure ai search**
* **langchain**
* **pymupdf4llm**
* **uv**

## project structure

```text
investorlens/
├── docs/
├── ingestion/
├── llm/
├── vectorstore/
├── .dockerignore
├── .gitignore
├── project_journey.md
├── README.md
└── requirements.txt
```

## documentation

* **brd** — business requirements
* **prd** — product requirements
* **trd** — technical requirements
* **architecture diagrams**
* **project journey**

see `docs/` and `project_journey.md` for the complete project documentation.

## what's next

the upcoming phases include:

* kpi extraction
* database integration
* fastapi backend
* frontend
* rag research pipeline
* containerization
* aks deployment

these features are planned and are not part of the current implementation.

---

see you in the next phase.

— aps