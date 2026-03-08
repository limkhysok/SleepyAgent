# 💤 SleepyAgent

> **Stealth Orchestrator:** Local-First AI Content Generation & Residential IP Automation.

SleepyAgent is a professional-grade desktop suite built for creators who want to automate social media growth without the risks of cloud-based tools. By leveraging your **Local Residential IP** and **On-Premise AI**, SleepyAgent avoids the common "Shadow-bans" and "Bot Flags" associated with server-side automation like n8n or Zapier.

---

## 🌟 Why SleepyAgent?

* **Residential Trust:** Posts originate from your home ISP, not a flagged data center (AWS/Google Cloud).
* **Privacy First:** Your API tokens and media files never leave your machine.
* **Zero Subscription:** Use your own GPU to generate videos and images for free.
* **Human Mimicry:** Built-in "Jitter" algorithms and metadata scrubbing simulate manual activity.

---

## 🚀 Core Workflows

### 🛠 Pipeline I: The Stealth Publisher
*Focus: Safe, high-trust deployment of existing or generated content.*

1.  **Secure OAuth2 Loopback:** Authenticate via a local browser handshake. Tokens are stored in an encrypted local vault.
2.  **Metadata Laundering:** Every file passes through a local **FFmpeg** worker to strip tracking metadata and randomize file headers.
3.  **The Residential Advantage:** API requests bypass the "Commercial IP" filters that social platforms use to identify bots.
4.  **Smart-Jitter Scheduling:** Posts are deployed with randomized time offsets to mimic human behavior patterns.

### 🤖 Pipeline II: The Agentic Producer
*Focus: One-prompt content creation using local hardware.*

1.  **Concept Engine (Ollama):** Local LLMs (Llama 3 / DeepSeek) expand a single prompt into a script, tags, and SEO metadata.
2.  **Visual Forge (LTX-2 / FLUX):** Generates cinematic video clips and high-CTR thumbnails directly on your GPU.
3.  **Auto-Assembly:** Background workers stitch assets, overlay audio, and burn subtitles into the final .mp4.
4.  **Human-in-the-loop:** Review and approve the "Draft" in the PyQt6 Dashboard before it enters the publishing queue.

---

## 🏗 Technical Stack

| Layer | Technology |
| :--- | :--- |
| **GUI** | PyQt6 (Asynchronous / Multi-threaded) |
| **Automation** | Google YouTube Data API v3 / Facebook Graph API |
| **Intelligence** | Ollama (Llama 3 / Mistral) |
| **Visuals** | LTX-Video / FLUX.1-dev (via local Diffusers) |
| **Processing** | FFmpeg (Metadata scrubbing & Video editing) |
| **Security** | Python-dot-env & Local OAuth2 Handlers |

---

## 📂 Project Structure

```text
SleepyAgent/
├── assets/             # AI generated images/videos
├── core/
│   ├── ai_agent.py     # Ollama & Image Gen logic
│   ├── api_handler.py  # YouTube/FB API integration
│   └── video_edit.py   # FFmpeg assembly scripts
├── ui/
│   ├── main_window.py  # PyQt6 Dashboard
│   └── components.py   # Custom widgets & Progress bars
├── .env                # Local API Keys (DO NOT SHARE)
├── main.py             # Entry point
└── README.md
