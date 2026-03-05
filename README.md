<div align="center">

# 🎬 Animated Slides Pipeline

**Type a topic. Get a cinematic AI presentation.**

[![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=flat&logo=python&logoColor=white)](https://python.org)
[![Gemini](https://img.shields.io/badge/Gemini-2.5_Flash-4285F4?style=flat&logo=google&logoColor=white)](https://ai.google.dev)
[![Imagen](https://img.shields.io/badge/Imagen-4.0-34A853?style=flat&logo=google&logoColor=white)](https://ai.google.dev)
[![Kling](https://img.shields.io/badge/Kling-2.1_Pro-FF6B35?style=flat)](https://fal.ai)
[![License](https://img.shields.io/badge/License-MIT-00d4c8?style=flat)](LICENSE)

<br>

```
python main.py "How to Build AI Agents" my-deck
```

*→ 10 AI-generated slides + cinematic morph transitions + offline HTML player*

</div>

---

## ⚡ How It Works

```
TOPIC STRING
    │
    ▼
┌─────────────────────────────────────────────────────┐
│  Stage 1  │  Gemini 2.5 Flash  │  slides.json        │
│  Stage 2  │  Imagen 4          │  slide_01..10.png   │
│  Stage 3  │  Kling 2.1 Pro     │  t_01_02..mp4       │
│  Stage 4  │  Pure Python       │  player.html ✓      │
└─────────────────────────────────────────────────────┘
    │
    ▼
output/my-deck/player.html   ← double-click. done.
```

> `player.html` is fully self-contained — images + videos base64-embedded. No server. No internet. Works on a plane.

---

## 🚀 Setup

```bash
git clone https://github.com/100x-Engineers100/animated-slides-pipeline.git
cd animated-slides-pipeline

python -m venv venv && venv\Scripts\activate   # Windows
# OR: source venv/bin/activate                 # Mac/Linux

pip install -r requirements.txt
cp .env.example .env   # add your API keys
```

**Keys needed** — both free to sign up:
| Key | Where |
|---|---|
| `GEMINI_API_KEY` | [aistudio.google.com/apikey](https://aistudio.google.com/apikey) |
| `KLING_API_KEY` | [fal.ai/dashboard](https://fal.ai/dashboard) |

> Billing must be enabled on Google Cloud for Imagen 4.

---

## 🎮 Usage

```bash
# Full pipeline
python main.py "The Future of AI" my-deck

# No transitions (faster, cheaper)
python main.py "Deep Learning" ml-deck --skip-transitions

# Slides only (free)
python main.py "Blockchain" crypto-deck --slides-only

# Switch to Gemini image gen instead of Imagen 4
python main.py "Web3" web3-deck --image-backend gemini
```

---

## 🎥 Player Controls

| Key | Action |
|---|---|
| `SPACE` / `→` | Next slide + morph transition |
| `←` | Previous slide |
| `G` | Grid overview |
| `P` | View AI prompts used |
| `F` | Fullscreen |
| `ESC` | Close panel |

---

## 💰 Cost Per Deck

| Stage | Cost |
|---|---|
| Slides JSON | ~$0.00 |
| 10 images (Imagen 4) | ~$0.10–0.20 |
| 9 transitions (Kling) | ~$1.25–2.50 |
| **Total** | **~$1.35–2.70** |

> Use `--skip-transitions` to skip Kling entirely and keep it under $0.25.

---

## 🔁 Resume Interrupted Runs

Already generated files are **automatically skipped**. If the pipeline crashes on image 6, re-run the same command — it picks up from image 7.

---

<div align="center">

Built by [@vishal2903](https://github.com/vishal2903)

</div>
