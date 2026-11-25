# DocuScan AI Agent

Autonomous document intelligence agent built for parsing, analyzing, and answering multi-turn queries across complex PDF documents. Powered by PyMuPDF, LiteLLM, and Chainlit for conversational document interactions.

---

### Architecture & Capabilities

- **Document Parsing Engine:** High-fidelity text and layout extraction using PyMuPDF (`fitz`).
- **Context Routing & Memory:** Session-scoped context storage with persistent multi-turn conversational history.
- **Model Agnostic Backend:** LLM completions managed via LiteLLM targeting Google Gemini with strict schema enforcement.
- **Conversational Interface:** Responsive streaming web UI powered by Chainlit with file drop upload.

---

### Project Structure

```text
├── main.py              # Application entry point, session lifecycle, and Chainlit handlers
├── pyproject.toml       # Python package configuration and dependencies
├── requirements.txt     # Locked production dependencies
├── Procfile             # Deployment configuration for production hosts
├── .env.example         # Environment variable template
└── chainlit.md          # Chainlit session header configuration
```

---

### Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Yusra-Saleem/DocuScan-AI-Agent.git
   cd DocuScan-AI-Agent
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment:**
   ```bash
   cp .env.example .env
   # Add your GEMINI_API_KEY to .env
   ```

5. **Run the application:**
   ```bash
   chainlit run main.py -w
   ```

---

### License

MIT License. Designed and maintained by Yusra Saleem.
