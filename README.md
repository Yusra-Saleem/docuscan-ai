# DocuScan Autonomous OCR & Document Agent

> Autonomous document intelligence, layout-aware OCR parsing, and context routing agent powered by multimodal vision and LLM parsing.

## 1. System Overview

DocuScan AI is an autonomous document processing agent designed to eliminate manual data entry from complex business documents. It ingests invoices, receipts, regulatory forms, and technical manuals, leverages multimodal vision models for layout analysis, extracts structured Pydantic schemas, and routes normalized records into backend databases.

## 2. Technical Architecture

```
[ Unstructured Document (PDF / Image) ]
        │
        ▼
[ Multimodal Vision OCR Engine ]
        │
        ▼
[ Layout Analysis & Semantic Chunking ]
        │
        ▼
[ LLM Extraction & Pydantic Validation ]
        │
        ▼
[ Normalized JSON Schema + Context Router ]
```

### Technology Stack
- **Core Runtime:** Python 3.10+
- **Vision & LLM:** Google Gemini Multimodal Vision API
- **Interface:** Chainlit interactive document workbench (`chainlit.md`, `.chainlit/`)
- **Package Management:** uv / pyproject.toml
- **Deployment:** Procfile ready for cloud container runtimes

## 3. Core Functional Capabilities

- **Layout-Aware Extraction:** Identifies and parses tabular line items, tax subtotals, vendor metadata, and dates from unstructured documents.
- **Strict Schema Enforcement:** Validates extracted fields against Pydantic models with automated type coercion and missing field flags.
- **Interactive Workbench:** Chainlit-powered visual chat interface allowing operators to upload documents and inspect extraction confidence scores.
- **Security Hardening:** Sanitized `.env.example` templates; zero API keys committed to version control.

## 4. Directory Structure

```
docuscan-ai/
├── main.py                   # Document processing engine and entry point
├── chainlit.md               # Interactive UI branding and workbench layout
├── pyproject.toml            # Modern Python package dependencies
├── requirements.txt          # Standard pip dependency manifest
├── Procfile                  # Production cloud deployment directive
└── .env.example              # Sanitized environment configuration
```

## 5. Getting Started

```bash
git clone https://github.com/Yusra-Saleem/docuscan-ai.git
cd docuscan-ai

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

pip install -r requirements.txt
cp .env.example .env

chainlit run main.py -w
```

## 6. Author and License

- **Author:** Yusra Saleem
- **Portfolio:** [yusrasaleem.dev](https://yusrasaleem.dev)
- **License:** Licensed under the [MIT License](LICENSE).
<!-- timeline-sync -->
<!-- updated: 2026-11-26T14:07:17Z -->
