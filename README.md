# 💬 SentimentLens — NLP Analyser

> Classify emotion, intent, and urgency in any text — powered by real transformer models, running entirely in your browser. No API key. No server. No cost.

![Status](https://img.shields.io/badge/status-live-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Models](https://img.shields.io/badge/models-DistilBERT%20%7C%20RoBERTa-8b5cf6)
![Zero API](https://img.shields.io/badge/API%20key-not%20required-success)
![Works Offline](https://img.shields.io/badge/offline-capable-orange)

---

## 🌐 Live Demo

👉 **[gorickroot.github.io/sentimentlens](https://gorickroot.github.io/sentimentlens)**

---

## 📸 Preview

![SentimentLens Preview](./preview.png)

---

## ✨ What It Does

SentimentLens runs a full NLP pipeline directly in your browser — no backend, no API key, no data ever leaves your device.

Paste any customer review, social post, or support message and get instant analysis across 5 dimensions:

| Output | Description |
|--------|-------------|
| 😤 **Emotion** | Joy, Anger, Frustration, Fear, Disgust, Surprise, Sadness, Neutral |
| 🎯 **Intent** | Complaint, Praise, Request, Feedback, Report, Threat, Neutral |
| 🚨 **Urgency** | Low / Medium / High / Critical with confidence score |
| 📊 **Sentiment** | Positive / Negative / Neutral / Mixed (−1.0 to +1.0) |
| 🔑 **Keywords** | Top 5 extracted key terms |
| 🧠 **Summary** | Professional 2-sentence NLP insight |
| 📋 **Response Priority** | Normal / High / Urgent — tells teams who to reply to first |

---

## 🧠 How It Works

```
User Input (text)
      │
      ▼
Transformers.js (ONNX Runtime — WebAssembly)
      ├── DistilBERT SST-2       → Sentiment polarity + score
      ├── Multilingual BERT      → Star rating → emotion mapping
      ├── Rule-based engine      → Urgency scoring (keywords + caps + punctuation)
      └── TF-IDF extractor       → Top keywords
      │
      ▼
Rendered UI — animated cards, progress bars, priority badge
```

All models download once (~20MB), are cached in your browser, and run **fully offline** after that.

---

## 🚀 Getting Started

### Just open it
```
Download index.html → double-click → runs instantly in any browser
```

### Or clone it
```bash
git clone https://github.com/gorickroot/sentimentlens.git
cd sentimentlens
open index.html
```

No `npm install`. No build step. No config. Just open and go.

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Runtime | Transformers.js v2 + ONNX WebAssembly |
| Sentiment model | `distilbert-base-uncased-finetuned-sst-2-english` |
| Emotion model | `bert-base-multilingual-uncased-sentiment` |
| Urgency scoring | Custom rule-based NLP engine |
| Keyword extraction | TF-IDF inspired local algorithm |
| Frontend | Vanilla HTML, CSS, JavaScript (zero dependencies) |
| Fonts | DM Sans · DM Mono · Fraunces (Google Fonts) |
| Deployment | GitHub Pages |

---

## 📂 Project Structure

```
sentimentlens/
│
├── index.html      ← Entire app lives here (models + UI + logic)
├── README.md       ← You're reading it
└── preview.png     ← Screenshot for README / portfolio
```

---

## 💡 Use Cases

- **Customer support teams** — prioritise tickets by urgency automatically
- **Social media monitoring** — understand the emotional tone of brand mentions
- **E-commerce** — detect frustrated buyers before they churn
- **Product teams** — classify user feedback at scale
- **HR & internal comms** — gauge urgency and emotion in employee messages

---

## 🧪 Example Inputs to Try

**Angry review:**
```
I've been a loyal customer for 3 years and this is absolutely disgraceful.
My order arrived broken AGAIN and customer service keeps giving me the runaround.
```

**Urgent support ticket:**
```
URGENT: Our entire production system is down. We are losing thousands per minute
and your support line has had me on hold for 45 minutes. Fix this IMMEDIATELY.
```

**Happy post:**
```
Just got my new headphones and WOW. Sound quality is incredible, delivery was
super fast, packaging was beautiful. 10/10 would recommend to absolutely everyone!
```

---

## 📈 Roadmap

- [ ] Batch mode — paste multiple texts, analyse all at once
- [ ] CSV upload — run analysis across hundreds of rows
- [ ] Export results as PDF / CSV
- [ ] Trend dashboard — chart sentiment over time
- [ ] Chrome extension — analyse selected text on any page
- [ ] Multi-language support (Arabic, Spanish, French)
- [ ] Python/Flask backend with full BERT + spaCy pipeline

---

## 🌐 Works In

![Chrome](https://img.shields.io/badge/Chrome-✓-green)
![Edge](https://img.shields.io/badge/Edge-✓-green)
![Firefox](https://img.shields.io/badge/Firefox-✓-green)
![Safari](https://img.shields.io/badge/Safari-✓-green)

---

## 👨‍💻 Author

**Gorick Nath**
BSc Computing Science — Griffith College Dublin, Ireland 🇮🇪

Building AI agents & automations 🤖 · Founding ZynthoAI

> *"Every line of code is a step forward."*

[![Portfolio](https://img.shields.io/badge/Portfolio-gorickroot.github.io-2d6a4f?style=flat&logo=google-chrome&logoColor=white)](https://gorickroot.github.io)
[![GitHub](https://img.shields.io/badge/GitHub-gorickroot-181717?style=flat&logo=github)](https://github.com/gorickroot)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-gorick--nath--aigeek-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/gorick-nath-aigeek)

---

*This project is part of my developer portfolio. Feel free to fork and build on it!*

---

## 📄 License

MIT License — free to use, modify, and distribute.
