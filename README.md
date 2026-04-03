# 💊 MedLingo – AI-Powered Medicine Explainer

> **Codecure · SPIRIT 2026** — IIT (BHU) Varanasi Annual Techno-Pharma Conference

---

## 📌 Project Overview

**MedLingo** is an AI-driven health literacy tool that empowers patients and caregivers to understand their medicines in simple, plain language — in their own native language.

Users simply type a medicine name and instantly receive a structured breakdown covering:
- What the medicine is used for
- How it works in the body
- Common side effects
- Dosage guidance
- Warnings & precautions
- A patient-friendly tip

The tool supports **5 Indian languages** (English, Hindi, Bengali, Tamil, Telugu), making it accessible to patients across rural and urban India.

---

## 🛠️ Tech Stack & Tools

| Layer | Technology |
|---|---|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| AI Engine | Claude AI API (`claude-sonnet-4-20250514`) |
| Hosting | GitHub Pages (zero-config deployment) |
| Fonts | Google Fonts (Fraunces + DM Sans) |

> No backend, no server, no installation required. Runs entirely in the browser.

---

## 🚀 Installation & Setup

### Option 1 – Run Locally (Simplest)
```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/medlingo.git

# 2. Open in browser
open index.html
# OR just double-click index.html
```

### Option 2 – Deploy on GitHub Pages (Recommended)
1. Push the repository to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch → `/ (root)`
4. Your app is live at `https://YOUR_USERNAME.github.io/medlingo`

> **Note:** The Claude API is called directly from the browser. No API key is needed when running via GitHub Pages with the provided configuration.

---

## ✨ Features

- 🔍 **Medicine Search** — Instant AI-powered explanations for any medicine
- 🌐 **Multilingual Support** — Responses in English, Hindi, Bengali, Tamil, Telugu
- 📋 **Structured Output** — Uses, mechanism, side effects, dosage, warnings, tips
- ⚡ **Quick Search Pills** — One-click common medicines (Paracetamol, Metformin, etc.)
- 📱 **Fully Responsive** — Works on mobile, tablet, desktop
- ⚠️ **Medical Disclaimer** — Built-in safety messaging on every result
- 🎨 **Clean UI** — Warm editorial design, no clutter

---

## 🔧 Technical Workflow

```
User Input (Medicine Name + Language)
        │
        ▼
Structured Prompt Construction
  → Instructs Claude to respond only in selected language
  → Requests JSON output with 8 structured fields
        │
        ▼
Claude AI API Call (claude-sonnet-4-20250514)
  → POST /v1/messages
  → Returns structured JSON
        │
        ▼
Response Parsing & Rendering
  → Parse JSON from AI response
  → Render cards: Use, Mechanism, Side Effects,
    Dosage, Warnings, Patient Tip
        │
        ▼
User sees plain-language medicine explanation
```

### System Architecture

```
index.html (Single File Application)
├── HTML Structure — Search UI + Result Cards
├── CSS — Responsive layout, animations, theming
└── JavaScript
    ├── Language selector state
    ├── Prompt engineering (structured JSON request)
    ├── Anthropic API fetch call
    ├── JSON parsing & error handling
    └── Dynamic DOM rendering
```

---

## 🌍 Problem Statement Addressed

> **Health Literacy Gap in India:** Over 65% of Indian patients cannot correctly read or understand their medicine labels. Lack of health literacy leads to incorrect dosage, missed side effect identification, and dangerous drug interactions — especially in rural and semi-urban populations.

**MedLingo** bridges this gap by converting complex pharmacological information into simple, accessible language — in the patient's own mother tongue.

---

## 📈 Scalability

- **Offline Mode** (future): Cache common medicines via Service Workers
- **Voice Input/Output** (future): Web Speech API for low-literacy users
- **Pharmacy Integration** (future): Scan medicine barcode → auto-explain
- **WhatsApp Bot** (future): Reach users with no smartphones via messaging
- **Doctor Dashboard** (future): Bulk patient education materials

---

## 👥 Team

| Name | Role |
|---|---|
| Member 1 | Frontend + UI Design |
| Member 2 | AI Integration + Prompt Engineering |
| Member 3 | Research + Documentation |
| Member 4 | Testing + Deployment |

---

## 📄 License

MIT License — Free to use, modify, and distribute for educational purposes.

---

*Built with ❤️ for Codecure · SPIRIT 2026 — IIT (BHU) Varanasi*
