# Agents & Tools 🤖⚡

> A deep-dive notebook series exploring **LangChain 1.x** capabilities — from building your first agent to mastering structured outputs, multi-provider model integration, and production-grade middleware patterns.

---

## 📚 Notebook Series

| # | Notebook | Topics Covered |
|---|----------|---------------|
| 01 | `01_intro_and_agents.ipynb` | LangChain v1 intro · Agent creation · Tool calling loop |
| 02 | `02_model_integration.ipynb` | OpenAI · Google Gemini · Groq multi-provider integration |
| 03 | `03_tools.ipynb` | Tool schemas · Tool execution loops · Custom tool functions |
| 04 | `04_messages.ipynb` | Message types · Roles & metadata · Text/multi-modal prompts |
| 05 | `05_structured_output.ipynb` | Pydantic schemas · JSON enforcement · Parsed output alongside messages |
| 06 | `06_middleware.ipynb` | Logging · Summarization middleware · Token limits · Guardrails |

---

## 🗂️ Workspace Structure

```text
02_agents_and_tools/
├── 01_intro_and_agents.ipynb    # Agents & tool-calling basics
├── 02_model_integration.ipynb   # OpenAI, Gemini, Groq integrations
├── 03_tools.ipynb               # Custom tools & execution loops
├── 04_messages.ipynb            # LangChain message system deep-dive
├── 05_structured_output.ipynb   # Pydantic-enforced structured responses
├── 06_middleware.ipynb          # Middleware, summarization & guardrails
├── main.py                      # Standalone script entry point
├── requirements.txt             # pip-based dependencies
├── pyproject.toml               # uv project configuration
└── .python-version              # Pinned Python version (3.12)
```

---

## 🧠 What You'll Learn

### 01 — Intro & Agents
Get hands-on with **LangChain 1.x** by building your first agent from scratch. Understand the `create_agent` API, wire up custom Python functions as tools, and watch the agent reason, call tools, and return grounded answers via the message loop.

### 02 — Multi-Provider Model Integration
Switch seamlessly between **OpenAI GPT**, **Google Gemini**, and **Groq** using LangChain's unified model interface. Learn how to configure each provider, manage API keys, and benchmark response quality side by side.

### 03 — Tools
Understand tools as first-class LangChain citizens — composed of a **schema** (name, description, argument types) and a **callable**. Build tools that fetch data, run code, or query APIs, then wire them into an agent with a proper **execution loop**.

### 04 — Messages
Dive into LangChain's message system — the backbone of every LLM conversation. Explore `HumanMessage`, `AIMessage`, `ToolMessage`, and `SystemMessage`, understand roles and metadata, and learn how to handle **text, image, and multi-modal** content uniformly across all model providers.

### 05 — Structured Output
Force models to return machine-readable responses using **Pydantic schemas** and LangChain's `.with_structured_output()` API. Covers field validation, nested structures, optional fields, and extracting parsed output alongside the raw message for full traceability.

### 06 — Middleware
Add production-grade control over your agent with **middleware** — interceptors that run before/after model calls. Topics include:
- 🔍 Logging & analytics
- 📝 Conversation summarization (token-aware compression of old history)
- ⛔ Guardrails, rate limiting & PII detection
- 🔁 Retries and fallback logic

---

## ⚙️ Setup

### Prerequisites
- Python **3.12+**
- [`uv`](https://docs.astral.sh/uv/) (recommended) **or** `pip`

### 1. Install dependencies

**Using `uv` (recommended):**
```bash
uv sync
```

**Using `pip`:**
```bash
pip install -r requirements.txt
```

### 2. Configure API Keys

Create a `.env` file in this directory:

```dotenv
OPENAI_API_KEY=your_openai_key_here
GOOGLE_API_KEY=your_google_gemini_key_here
GROQ_API_KEY=your_groq_key_here
```

> **Tip:** You don't need all three keys — use only the provider(s) you intend to run.

| Provider | Where to Get |
|----------|-------------|
| OpenAI | [platform.openai.com/api-keys](https://platform.openai.com/api-keys) |
| Google Gemini | [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey) |
| Groq | [console.groq.com/keys](https://console.groq.com/keys) |

### 3. Open in Jupyter

```bash
# VS Code — open any .ipynb file and select the .venv kernel
# or
jupyter notebook
```

---

## 🚀 Recommended Learning Path

```
01_intro_and_agents  →  02_model_integration  →  03_tools
                                                       ↓
             06_middleware  ←  05_structured_output  ←  04_messages
```

Start from notebook `01` and work sequentially — each notebook builds on concepts from the previous one.

---

## 📦 Dependencies

```
langchain              # Core framework (v1.x)
langchain-community    # Community integrations
langchain-openai       # OpenAI provider
langchain-groq         # Groq provider
langchain-google-genai # Google Gemini provider
python-dotenv          # .env file loading
ipykernel              # Jupyter kernel support
```

---

## 🔑 Key Concepts at a Glance

| Concept | LangChain Class / Function |
|---------|---------------------------|
| Agent | `create_agent()` |
| Tool | `@tool` decorator / function schema |
| Messages | `HumanMessage`, `AIMessage`, `ToolMessage` |
| Structured Output | `.with_structured_output(PydanticModel)` |
| Middleware | `BaseCallbackHandler` / custom middleware |
| Multi-provider LLM | `ChatOpenAI`, `ChatGoogleGenerativeAI`, `ChatGroq` |

---

## 🗒️ Notes

- LangChain version used: **1.3.11** (see `01_intro_and_agents.ipynb` output)
- All notebooks are self-contained — cells are designed to run top-to-bottom
- The `.venv` directory is created by `uv` and should not be committed (covered by `.gitignore`)
- `main.py` serves as a minimal standalone script for quick CLI experiments
