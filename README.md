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



## 📂 Project Structure

```text
SleepyAgent/
├── assets/
│   ├── icons/              # SVG/PNG icons for buttons
│   ├── fonts/              # Custom typography (e.g., Inter, Roboto)
│   └── images/             # Branding and placeholder graphics
├── core/
│   ├── ai_engine/          # Local AI orchestration
│   │   ├── ollama_client.py   # Script & metadata generation
│   │   └── diffuser_gen.py    # Image/Video model connectors
│   ├── automation/         # Posting logic
│   │   ├── youtube_worker.py  # YT Data API v3 implementation
│   │   └── facebook_worker.py # Meta Graph API implementation
│   └── services/           # External integrations
│       ├── oauth_handler.py   # Google OAuth2 Loopback flow
│       └── config_manager.py  # Manages User API Keys & .env
├── ui/
│   ├── layouts/            # QSS (CSS) stylesheets & layout configs
│   ├── widgets/            # Reusable UI components (Buttons, Inputs)
│   │   └── components.py      # Custom QtWidgets
│   └── windows/            # Main Page logic
│       ├── dashboard.py       # Main view
│       ├── auth_page.py       # Login & API Setup page
│       └── ai_studio.py       # AI Prompt & Generation page
├── utils/                  # Helper functions (FFmpeg, File I/O)
├── main.py                 # Application entry point
├── requirements.txt        # Dependencies
└── .env                    # Local sensitive data

```
## 📜 License
Distributed under the MIT License. See `LICENSE` for more information.
---
