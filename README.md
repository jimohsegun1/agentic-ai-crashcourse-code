# Agentic AI Crash Course

Welcome to the Agentic AI Crash Course. This tutorial folder contains resources and examples to help you learn the basics of building agentic AI systems.

## Contents

| Folder | Topic |
|--------|-------|
| `1_simple_llm_calling` | Simple LLM API calls |
| `2_health_analysis` | Health data analysis agent |
| `3_vector_db` | Vector databases with ChromaDB |
| `4_rag_basics` | Retrieval-Augmented Generation (RAG) |
| `5_single_agent` | Single agent workflows |
| `6_memory` | Agent memory patterns |
| `7_multimodal` | Multimodal (vision + text) agents |
| `8_guardrails` | Safety and guardrails |
| `9_eval` | Agent evaluation |
| `10_project_shopping_agent` | Project: Shopping agent |
| `11_project_telecom_chatbot` | Project: Telecom RAG chatbot |

## Setup

### Prerequisites

- Python 3.14+
- [uv](https://docs.astral.sh/uv/) (recommended) or pip

#### Installing `uv`

**Via pip:**
```bash
pip install uv
```

> **Note (Windows):** If running `uv` directly returns "command not found" right after installation, ensure `C:\Users\<user>\AppData\Roaming\Python\Python313\Scripts` is in your `PATH`, restart your terminal, or invoke it with `python -m uv`:
> ```powershell
> python -m uv --version
> ```

**Via standalone installer (alternative):**
- **Windows (PowerShell):**
  ```powershell
  powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
  ```
- **macOS / Linux:**
  ```bash
  curl -LsSf https://astral.sh/uv/install.sh | sh
  ```

### 1. Clone the repository

```bash
git clone <repo-url>
cd agentic-ai-crash-course
```

### 2. Create and activate a virtual environment

**Using uv (recommended):**
```bash
uv sync
# Or if PATH has not reloaded in the current terminal:
python -m uv sync
```

**Using pip:**
```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate

pip install -e .
```

### 3. Configure API keys

Create `.env` from `.env.sample`:

```bash
# Windows (PowerShell)
Copy-Item .env.sample .env

# macOS / Linux
cp .env.sample .env
```

Open `.env` and set your keys:

```env
GOOGLE_API_KEY=your_google_api_key_here
GROQ_API_KEY=your_groq_api_key_here
LANGSMITH_API_KEY=your_langsmith_api_key_here
```

#### How to obtain your API keys:

1. **Google API Key (`GOOGLE_API_KEY`)** — *Used for Gemini and Gemma models in modules 1 and 2*:
   - Sign in to [Google AI Studio](https://aistudio.google.com/).
   - Click **Get API key** in the left sidebar.
   - Click **Create API key** (in a new or existing project) and copy the generated key (`AIzaSy...`).

2. **Groq API Key (`GROQ_API_KEY`)** — *Used for high-speed inference (Qwen & Llama models) across modules 4–11*:
   - Sign in to [Groq Console](https://console.groq.com/).
   - In the sidebar, select **[API Keys](https://console.groq.com/keys)**.
   - Click **Create API Key**, provide an optional label, and copy your key immediately (`gsk_...`).

3. **LangSmith API Key (`LANGSMITH_API_KEY`)** — *Optional, used for agent tracing and evaluations in module 9*:
   - Sign in to [LangSmith](https://smith.langchain.com/).
   - Click the **Settings (gear icon)** at the bottom-left of the sidebar.
   - Under the **API Keys** tab, click **Create API Key** and copy your key (`lsv2_...`).

### 4. Run the notebooks

Launch Jupyter and open any notebook from the numbered folders:

```bash
jupyter notebook
```

Or run Streamlit apps (where applicable):

```bash
streamlit run <folder>/app.py
```

## Getting Started

1. Start with `1_simple_llm_calling` to verify your setup.
2. Work through the numbered folders in order.
3. Explore the project folders (`10_*`, `11_*`) to see complete end-to-end examples.

## Notes

This course is designed for quick learning and practical application of agentic AI techniques.

Codebasics Inc all rights reserved