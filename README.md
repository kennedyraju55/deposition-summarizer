# ⚖️ Deposition Summarizer

Summarize legal depositions with AI-powered analysis

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Ollama](https://img.shields.io/badge/Ollama-Compatible-blue)](https://ollama.com/)
[![Gemma 3](https://img.shields.io/badge/Gemma%203-Powered-teal)](https://ollama.com/library/gemma3)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Privacy First](https://img.shields.io/badge/Privacy-First-brightgreen)](https://www.gnu.org/philosophy/privacy.html)

## What It Does

- Analyzes and summarizes deposition transcripts using Gemma 3
- Extracts key testimony, contradictions, and critical statements
- Generates executive summaries and detailed analysis reports
- Keeps all data private and secure with local processing

## Tech Stack

- **Language**: Python 3.8+
- **LLM**: Gemma 3 via [Ollama](https://ollama.com/)
- **Web Framework**: Streamlit (UI), FastAPI (API backend)
- **Processing**: Local, entirely on your machine
- **Privacy**: No data leaves your system

## Quick Start

### Prerequisites
- Python 3.8+
- [Ollama](https://ollama.com/) installed and running

### Installation

\\\ash
# Clone the repository
git clone https://github.com/kennedyraju55/deposition-summarizer.git
cd deposition-summarizer

# Install dependencies
pip install -r requirements.txt

# Pull the Gemma 3 model
ollama pull gemma3:4b

# Run the application
streamlit run app.py
\\\

The application will open at \http://localhost:8501\

## Architecture

\\\
┌─────────────────────────────────────────────┐
│         User (Your Browser)                 │
└────────────────┬────────────────────────────┘
                 │
                 ▼
┌─────────────────────────────────────────────┐
│      Streamlit Frontend Interface           │
└────────────────┬────────────────────────────┘
                 │
                 ▼
┌─────────────────────────────────────────────┐
│      FastAPI Backend Service                │
└────────────────┬────────────────────────────┘
                 │
                 ▼
┌─────────────────────────────────────────────┐
│      Local Ollama Server                    │
│      └─ Gemma 3 Model                       │
└─────────────────────────────────────────────┘
                 │
                 ▼
        Response → User
\\\

## Why Local?

Running legal AI locally provides critical protections:

- **Attorney-Client Privilege**: Your documents never leave your control
- **GDPR & Data Privacy**: No cloud uploads, full compliance assured
- **Confidential Data**: Sensitive information stays on your hardware
- **Zero Latency**: Instant responses without network delays
- **Cost Effective**: No API fees or subscription charges
- **Offline Capability**: Works without internet connection

## Configuration

Configuration can be customized in the \.env\ file:

\\\nv
OLLAMA_BASE_URL=http://localhost:11434
MODEL_NAME=gemma3:4b
\\\

## Troubleshooting

### "Failed to connect to Ollama"
Ensure Ollama is running: \ollama serve\

### "Model not found"
Pull the model: \ollama pull gemma3:4b\

### Performance Issues
- Allocate more resources to Docker (if using)
- Reduce model context length in settings
- Use a faster hardware configuration

## Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch (\git checkout -b feature/amazing-feature\)
3. Commit your changes (\git commit -m 'Add amazing feature'\)
4. Push to the branch (\git push origin feature/amazing-feature\)
5. Open a Pull Request

## License

This project is licensed under the MIT License — see the [LICENSE](./LICENSE) file for details.

---

**Part of 114+ privacy-first AI tools by [Nrk Raju](https://github.com/kennedyraju55)**