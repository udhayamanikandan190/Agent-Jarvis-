# Agent-Jarvis-
A browser-based voice assistant (JARVIS) built with vanilla HTML, CSS &amp; JavaScript — opens websites, searches, calculates, tells time/jokes, and answers common questions using the Web Speech API. Installable as a PWA.
# JARVIS — Browser Voice Assistant 🎙️

A lightweight, no-backend voice assistant that runs entirely in the browser using vanilla **HTML, CSS, and JavaScript**. It listens to your voice (or typed text), talks back, and can open websites, run searches, do quick calculations, and answer common everyday questions — inspired by the ChatGPT-style chat interface.

Installable as a **Progressive Web App (PWA)**, so it can be added to your phone or desktop home screen like a native app.

---

## ✨ Features

- 🎙️ Voice input & spoken replies (Web Speech API — no external API keys needed)
- 💬 ChatGPT-style chat bubble interface with quick-suggestion chips
- 🌐 Opens YouTube, Google, Instagram, Facebook, WhatsApp, Gmail, Twitter/X, Spotify, Amazon, Netflix, LinkedIn
- 🔍 Google / YouTube / Wikipedia / dictionary search by voice or text
- 🗺️ Maps search, weather lookup
- 🧮 Quick calculator ("calculate 12 times 4")
- 🕒 Time & date
- 😄 Jokes, random facts, coin flip, dice roll
- 🙂 Everyday small talk (greetings, "how are you", "who made you", etc.)
- 🤷 Smart fallback — unknown questions are searched on Google automatically
- 📱 Installable as a PWA (offline shell + home-screen icon) via `manifest.json` + `sw.js`

## 🚀 Getting Started

No build tools or installation required — it's a static site.

### Run locally
```bash
# any static server works, e.g.
python3 -m http.server 8000
```
Open `http://localhost:8000/jarvis.html` in your browser.

### Deploy
Host the folder on any static host — **GitHub Pages**, **Netlify**, or **Vercel**. HTTPS is required for microphone access (localhost is exempt).

### Install as an app
1. Deploy the site over HTTPS.
2. Open it in Chrome (Android/desktop) or Safari (iOS).
3. Tap **"Add to Home Screen"** / **"Install app"**.
4. It now launches full-screen like a native app.

Want a real installable `.apk`? Paste your deployed HTTPS URL into [PWABuilder](https://www.pwabuilder.com) to generate one for free.

## 📁 Project Structure

```
├── jarvis.html      # Main app (UI + logic)
├── manifest.json    # PWA metadata (name, icons, theme)
├── sw.js            # Service worker (installability + offline cache)
├── icon-192.png     # App icon (small)
└── icon-512.png     # App icon (large)
```

## 🛠️ Tech Stack

- HTML5 / CSS3
- Vanilla JavaScript (no frameworks, no dependencies)
- Web Speech API (`SpeechRecognition` + `SpeechSynthesis`)
- Service Worker / Web App Manifest (PWA)

## 📌 Notes / Limitations

- Voice recognition requires a Chromium-based browser (Chrome, Edge) for best support.
- Microphone access requires HTTPS or `localhost`.
- All processing happens client-side — no server, no database, no API keys.

## 📄 License

MIT
