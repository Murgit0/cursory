# AGENTS.md

## Cursor Cloud specific instructions

This repository ("cursory") is a Python AI/ML toolkit with dependencies listed in `requirements.txt`.

### Setup

```bash
pip install --ignore-installed -r requirements.txt
```

The `--ignore-installed` flag is needed to avoid conflicts with Debian system-managed packages (e.g. `PyJWT`, `blinker`, `Jinja2`).

### Key dependency groups

| Category | Packages |
|---|---|
| LLM Clients | openai, anthropic, google-genai, cohere, mistralai, ollama, groq, together |
| Orchestration / RAG | langchain, langgraph, llama-index, crewai, autogen-agentchat, dspy |
| HF Ecosystem | transformers, datasets, accelerate, peft, tokenizers, sentence-transformers, trl |
| Deep Learning | torch (CPU), torchvision, torchaudio |
| Classical ML | scikit-learn, xgboost, lightgbm, catboost |
| NLP | spacy, nltk, tiktoken |
| Computer Vision | opencv-python-headless, pillow, ultralytics |
| Vector DBs | chromadb, faiss-cpu, qdrant-client, pinecone, weaviate-client |
| Data | numpy, pandas, scipy, polars |
| Viz | matplotlib, seaborn, plotly |
| MLOps | mlflow, wandb, tensorboard |
| App frameworks | gradio, streamlit |

### Caveats

- PyTorch is installed as CPU-only (`--index-url https://download.pytorch.org/whl/cpu`). No GPU available in Cloud Agent VMs.
- LLM provider clients (openai, anthropic, etc.) require API keys set as environment variables to make real API calls.
- No lint/test/build commands are configured yet — add them as the codebase grows.
