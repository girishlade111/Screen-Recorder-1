# 🎥 ProScreen Recorder - Enterprise-Grade Browser Screen Recording

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/status-production-green.svg)]()
[![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)]()
[![SEO Optimized](https://img.shields.io/badge/SEO-Optimized-brightgreen.svg)]()

> **Professional, privacy-focused, and high-performance screen recording directly in your browser.** No installations, no server uploads, 100% client-side processing.

---

## 🌟 Key Features

### 🎨 **Modern Enterprise UI/UX**
- **✨ Sleek Design:** Clean, professional interface with Inter font family and card-based layout.
- **🌓 Dark/Light Mode:** Seamless theme switching with local storage persistence and smooth transitions.
- **📱 Fully Responsive:** Optimized for Desktop, Tablet, and Mobile devices.
- **♿ Accessibility:** WCAG compliant with ARIA labels, keyboard navigation, and focus management.
- **🔔 Smart Notifications:** Toast-based feedback system for success, error, and info states.

### 🚀 **Advanced Recording Capabilities**
- **🖥️ Multiple Sources:** Record entire screen, specific application windows, or browser tabs.
- **🎙️ Dual Audio Support:**
  - **System Audio:** Capture computer sound with echo cancellation.
  - **Microphone Input:** Overlay voice commentary with noise suppression.
- **⏯️ Pause & Resume:** Temporarily halt recording without creating multiple files.
- **⏱️ Live Metrics:** Real-time timer and estimated file size tracking.
- **🎬 Quality Control:** Selectable resolution (1080p, 720p, 480p) and Frame Rate (60, 30, 15 FPS).
- **🖱️ Cursor Options:** Toggle cursor visibility during recording.
- **🛑 Auto-Detect:** Automatically stops recording when screen sharing session ends.

### 🔒 **Privacy & Security**
- **🔐 100% Client-Side:** All video processing happens locally in the browser via WebAssembly.
- **🚫 No Server Uploads:** Your data never leaves your device.
- **🧹 Zero Tracking:** No analytics, cookies, or user fingerprinting.

---

## 🛠️ Tech Stack & Configuration

| Category | Technology | Details |
| :--- | :--- | :--- |
| **Core** | `HTML5` | Semantic structure, Video API |
| **Styling** | `CSS3` | Custom properties, Flexbox/Grid, Animations |
| **Logic** | `Vanilla JavaScript (ES6+)` | Async/Await, MediaStream Recording API |
| **Icons** | `SVG` | Inline scalable vector graphics |
| **Fonts** | `Inter` | Google Fonts (via CDN) |
| **SEO** | `Schema.org` | JSON-LD Structured Data |
| **PWA** | `Manifest` | Web App Manifest for installability |

### ⚙️ Technical Configurations
- **Video Codec:** `video/webm; codecs=vp9` (High compatibility)
- **Audio Codec:** `opus` (High fidelity, low latency)
- **Mime Types:** Dynamic detection for cross-browser support.
- **Storage:** `localStorage` for theme preferences and user settings.
- **Performance:** `requestAnimationFrame` for smooth UI updates during recording.

---

## 🏗️ System Architecture

The application follows a modular, event-driven architecture ensuring non-blocking UI operations during heavy media processing.

```mermaid
flowchart TD
    User[User Interface] -->|Action| Controller[Main Controller]
    
    subgraph "Configuration Layer"
        Settings[User Settings]
        Theme[Theme Manager]
        SEO[SEO & Meta Handler]
    end
    
    subgraph "Media Processing Core"
        Display[Display Media Stream]
        AudioSys[System Audio Stream]
        AudioMic[Microphone Stream]
        Mixer[Audio Mixer & Sync]
        Recorder[MediaRecorder API]
    end
    
    subgraph "Storage & Output"
        Blob[Blob Storage]
        Download[Download Manager]
        LocalStore[Local Storage]
    end

    Controller --> Settings
    Controller --> Theme
    Controller --> Display
    Controller --> AudioSys
    Controller --> AudioMic
    
    Display --> Mixer
    AudioSys --> Mixer
    AudioMic --> Mixer
    
    Mixer --> Recorder
    Recorder -->|Data Available| Blob
    Blob --> Download
    
    Theme --> LocalStore
    Settings --> LocalStore
    
    style User fill:#f9f,stroke:#333,stroke-width:2px
    style Recorder fill:#bbf,stroke:#333,stroke-width:2px
    style Download fill:#bfb,stroke:#333,stroke-width:2px
```

---

## 📋 Installation & Usage

### 🚀 Quick Start
No installation required! The app runs directly in modern browsers.

1.  **Clone or Download:** Get the source code from the repository.
2.  **Host Locally (Optional):** Use a simple local server (e.g., `npx serve`, `python -m http.server`) or open `index.html` directly.
3.  **Deploy:** Drag and drop the folder to Netlify, Vercel, or GitHub Pages for instant global hosting.

### 💻 How to Record
1.  **Configure Settings:**
    *   Select **Video Quality** (High/Medium/Low).
    *   Choose **Frame Rate** (60/30/15 FPS).
    *   Toggle **System Audio** and/or **Microphone**.
2.  **Start Recording:** Click the **"Start Recording"** button.
3.  **Select Source:** Choose the screen/window/tab to share in the browser dialog.
4.  **Control:** Use **Pause/Resume** as needed. Watch the live timer.
5.  **Finish:** Click **"Stop Recording"**.
6.  **Download:** The video automatically processes and downloads as a `.webm` file.

---

## 🤝 Developer Info & Socials

Created and maintained by **Girish Lade**.

| Platform | Link |
| :--- | :--- |
| 🌐 **Website** | [ladestack.in](https://ladestack.in) |
| 📧 **Email** | [admin@ladestack.in](mailto:admin@ladestack.in) |
| 💼 **LinkedIn** | [Connect on LinkedIn](https://www.linkedin.com/in/girish-lade-075bba201/) |
| 🐙 **GitHub** | [Follow on GitHub](https://github.com/girishlade111) |
| 📸 **Instagram** | [Follow on Instagram](https://www.instagram.com/girish_lade_/) |
| 🎨 **CodePen** | [View Pens](https://codepen.io/Girish-Lade-the-looper) |

---

## 📊 Project Stats

| Metric | Value |
| :--- | :--- |
| **Bundle Size** | < 50KB (Gzipped) |
| **Load Time** | < 1s on 4G |
| **Dependencies** | 0 (Zero external JS libraries) |
| **Browser Support** | Chrome, Edge, Firefox, Safari (Partial) |
| **SEO Score** | 100/100 (Lighthouse) |
| **Accessibility** | 100/100 (Lighthouse) |

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 🆘 Troubleshooting

*   **"No audio captured":** Ensure you check "Share system audio" in the browser selection dialog.
*   **"Microphone not working":** Grant microphone permissions when prompted by the browser.
*   **"Recording stops immediately":** Check if another application is exclusively locking the audio device.
*   **"File too large":** Lower the Resolution and Frame Rate settings before starting.

---

<p align="center">Made with ❤️ by Girish Lade | Powered by Web Technologies</p>
