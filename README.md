# 💤 SleepyAgent

> **Stealth Orchestrator:** Local-First AI Content Generation & Residential IP Automation.

SleepyAgent is a professional-grade desktop suite built for creators who want to automate social media growth without the risks of cloud-based tools. By leveraging your **Local Residential IP** and **On-Premise AI**, SleepyAgent avoids the common "Shadow-bans" and "Bot Flags" associated with server-side automation like n8n or Zapier.

---

## 🚀 Core Workflows

### 🛡️ Pipeline I: The Stealth Publisher
*Focus: Safe, high-trust deployment via Residential IP.*

1.  **Secure OAuth2 Loopback:** Authenticate via a local browser handshake. Tokens are stored in an encrypted local vault.
2.  **API Integration:** User-provided Google API keys are validated locally for YouTube Data API v3 access.
3.  **Metadata Laundering:** Every file passes through a local **FFmpeg** worker to strip tracking metadata and randomize file headers.
4.  **The Residential Advantage:** API requests originate from your Home ISP, mimicking human behavior and maintaining a high trust score.

### 🤖 Pipeline II: The Agentic Producer
*Focus: One-prompt content creation using local hardware.*

1.  **Concept Engine (Ollama):** Local LLMs expand a single prompt into a script, tags, and SEO metadata.
2.  **Visual Forge (Local Diffusers):** Generates cinematic video clips and thumbnails directly on your GPU using LTX-Video and FLUX.
3.  **Auto-Assembly:** Background workers stitch assets, overlay audio, and burn subtitles into the final .mp4.
4.  **Review Dashboard:** A PyQt6-based "Studio" allows for final approval before the content is queued for posting.

---

## 🏗️ Technical Architecture

* **GUI Framework:** PyQt6 (Multithreaded with QThread)
* **Custom Widgets:** Modular QtWidgets and WindowPages for a sleek, modern UI.
* **External Services:** Google OAuth2 (Client-side), YouTube Data API v3.
* **AI Orchestration:** Ollama (LLM) + Local Diffusers (Video/Image).
* **Media Engine:** FFmpeg for metadata scrubbing and asset composition.

---

## 🛠️ Installation & Setup

1. **Clone the Repo:** `git clone https://github.com/your-username/SleepyAgent.git`
2. **Install Dependencies:** `pip install -r requirements.txt`
3. **Configure API:** Paste your Google Client Secrets and API Keys in the `auth_page.py` within the app.
4. **Launch:** `python main.py`

---

## 🛠️ Modern Tech Stack

| Component | Technology | Version |
| :--- | :--- | :--- |
| **Language** | Python | 3.12+ (Typed) |
| **GUI** | PyQt6 | 6.6+ (Asyncio integrated) |
| **Agents** | CrewAI / Pydantic-AI | Latest Agentic Frameworks |
| **Local LLM** | Ollama | Llama 3.2 / DeepSeek V3 |
| **Visuals** | Diffusers / LTX-Video | Torch 2.5+ (Cuda 12.x) |
| **Automation** | Playwright / Google-API | High-fidelity session control |

---

## ⚙️ Quick Start

1. **Prerequisites:** Install [Ollama](https://ollama.ai) and have an NVIDIA GPU (12GB+ VRAM recommended).
2. **Setup:** `pip install .` (using `pyproject.toml`)
3. **Environment:** Place your `client_secrets.json` in the `/core/security/` folder.
4. **Run:** `python main.py`

---

## 📂 Project Structure

```text
SleepyAgent/
├── assets/
│   ├── icons/              # Modern Lucide/Phosphor SVG icons
│   └── themes/             # QSS files for "Tokyo Night" or "Catppuccin" dark modes
├── core/
│   ├── agents/             # Agentic reasoning (The "Brain")
│   │   ├── planner.py         # CrewAI / LangGraph orchestration
│   │   └── tools.py           # Custom tools for agents to browse or edit files
│   ├── ai_stack/           # Local Model Interface
│   │   ├── ollama_py.py       # Async Ollama (Llama 3.2 / DeepSeek V3)
│   │   └── diffusers_v2.py    # Torch 2.5+ / Diffusers for LTX-Video & FLUX
│   ├── automation/
│   │   ├── google_api_v3.py   # Modern google-api-python-client (Async)
│   │   └── session_manager.py # Persistent secure browser sessions (Playwright)
│   └── security/
│       ├── oauth_pkce.py      # Modern PKCE flow for desktop security
│       └── vault.py           # Cryptography-based local token storage
├── ui/
│   ├── components/         # Custom QtWidgets (Modern, Rounded, Smooth)
│   ├── layouts/            # Fluid layouts using QGridLayout and QStackedWidget
│   └── pages/              # Logic for Dashboard, AI Studio, and Settings
├── main.py                 # Asyncio + PyQt6 entry point
└── pyproject.toml          # Modern dependency management (replacing requirements.txt)

```
## 📜 License
Distributed under the MIT License. See `LICENSE` for more information.
---
