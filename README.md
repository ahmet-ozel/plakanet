<p align="center">
  <img src="logo.png" alt="Plakanet - AI License Plate Recognition" width="180" />
</p>

<h1 align="center">Plakanet — AI-Powered License Plate Recognition</h1>

<p align="center">
  <strong>Real-time ANPR/LPR system for parking lots, gated communities, and site entrances</strong>
</p>

<p align="center">
  <a href="https://plakanet.net">🌐 Website</a> •
  <a href="https://plakanet.net/en/pricing">💰 Pricing</a> •
  <a href="https://plakanet.net/en/faq">❓ FAQ</a> •
  <a href="https://plakanet.net/en/features">⚡ Features</a> •
  <a href="https://apps.microsoft.com/detail/Plakanet">📦 Microsoft Store</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/platform-Windows%2010%2B-blue?logo=windows" alt="Platform" />
  <img src="https://img.shields.io/badge/.NET-8.0-purple?logo=dotnet" alt=".NET 8" />
  <img src="https://img.shields.io/badge/UI-WinUI%203-0078D4?logo=microsoft" alt="WinUI 3" />
  <img src="https://img.shields.io/badge/AI-ONNX%20Runtime-orange?logo=onnx" alt="ONNX" />
  <img src="https://img.shields.io/badge/GPU-DirectML-green?logo=nvidia" alt="DirectML" />
  <img src="https://img.shields.io/github/v/tag/ahmet-ozel/plakanet?label=version" alt="Version" />
</p>

---

## What is Plakanet?

**Plakanet** is a commercial AI-powered license plate recognition (LPR/ANPR) desktop application built for small businesses, parking facilities, and residential site entrances in Turkey and beyond.

It runs entirely on-premise with no cloud dependency for detection — your camera feeds never leave your machine.

## AI Models

| Task | Model | Architecture | Format |
|------|-------|-------------|--------|
| **Plate Detection** | YOLOv11n | YOLO v11 Nano | ONNX |
| **Character Recognition (OCR)** | CCT-S v1 Global | Compact Convolutional Transformer | ONNX |

- Both models run via **ONNX Runtime** with **DirectML** GPU acceleration (NVIDIA, AMD, Intel)
- CPU fallback available — no dedicated GPU required
- Optimized for Turkish plates with global plate format support
- Detection confidence threshold: configurable (default 0.5)
- OCR confidence threshold: configurable (default 0.6)

## Key Features

| Feature | Description |
|---------|-------------|
| 🤖 **AI Detection** | YOLOv11n real-time plate detection + CCT-S character recognition |
| 🏢 **Site Mode** | Authorized vehicle whitelist, entry/exit logging, unauthorized alerts |
| 🅿️ **Parking Mode** | Automatic duration-based fee calculation, occupancy tracking |
| 📷 **Multi-Camera** | Unlimited RTSP IP cameras and USB webcams, per-camera FPS control |
| ⚡ **Low Latency** | Lossless WriteableBitmap pipeline, RTSP TCP transport, frame buffer optimization |
| 📊 **Reports** | Daily/monthly access logs, revenue summaries, Excel export |
| 🔑 **Licensing** | 7-day free trial via [plakanet.net](https://plakanet.net), monthly/yearly subscriptions |
| 🌐 **Web Portal** | License management, user dashboard at [plakanet.net](https://plakanet.net) |
| 💻 **Windows Native** | WinUI 3 + .NET 8, MSIX packaging, Microsoft Store distribution |
| 🎯 **GPU Accelerated** | DirectML support for NVIDIA/AMD/Intel GPUs |
| 🔒 **Privacy First** | All processing on-premise, no cloud video upload |

## System Requirements

- Windows 10 version 1903 or later (x64)
- RTSP-compatible IP camera or USB webcam
- 8 GB RAM minimum (16 GB recommended for multi-camera)
- NVIDIA/AMD/Intel GPU recommended (DirectML compatible)
- CPU-only mode available for systems without dedicated GPU

## Installation

1. Download from [Microsoft Store](https://apps.microsoft.com/detail/Plakanet) or visit [plakanet.net](https://plakanet.net)
2. Launch → Get your free 7-day trial license at [plakanet.net/app/licenses](https://plakanet.net/app/licenses)
3. Setup wizard: choose mode (Site/Parking), configure cameras
4. Start the system

## Architecture

```
┌──────────────────────────────────────────────────┐
│  Desktop Application (WinUI 3 / .NET 8 / x64)    │
│  ├── Camera Service (RTSP TCP / USB / File)       │
│  ├── YOLOv11n Plate Detector (ONNX DirectML)     │
│  ├── CCT-S OCR Engine (ONNX DirectML)            │
│  ├── SQLite Database (EF Core)                    │
│  ├── Trigger & Automation Engine                  │
│  └── License Manager (online + offline cache)     │
└────────────────────┬─────────────────────────────┘
                     │ HTTPS
┌────────────────────▼─────────────────────────────┐
│  Web Platform — plakanet.net                      │
│  ├── Next.js 16 + TypeScript                     │
│  ├── Firebase Authentication                      │
│  ├── License API (trial, activation, renewal)     │
│  ├── Admin Dashboard                              │
│  └── Multi-language (TR/EN/DE/ES)                 │
└──────────────────────────────────────────────────┘
```

## Technology Stack

**Desktop:** .NET 8, WinUI 3, OpenCvSharp 4, ONNX Runtime (DirectML), Entity Framework Core, SQLite, Serilog, CommunityToolkit.Mvvm

**AI/ML:** YOLOv11 (Ultralytics), CCT (Compact Convolutional Transformer), ONNX format, DirectML execution provider

**Web:** Next.js 16, TypeScript, Tailwind CSS, Firebase Auth, SQLite (better-sqlite3), Caddy

**Infrastructure:** Docker, GitHub Actions CI/CD, MSIX packaging, Microsoft Store

## Pricing

| Plan | Price | Duration |
|------|-------|----------|
| Trial | Free | 7 days |
| Semi-Annual | $199 | 6 months |
| Annual | $349 | 12 months |

Details: [plakanet.net/pricing](https://plakanet.net/en/pricing)

## Links

- 🌐 **Website:** [plakanet.net](https://plakanet.net)
- 📦 **Microsoft Store:** [Download Plakanet](https://apps.microsoft.com/detail/Plakanet)
- 📧 **Contact:** info@plakanet.net
- 🏢 **Company:** [Valnox İnovasyon ve Reklam Promosyon A.Ş.](https://plakanet.net)

## License

This is proprietary commercial software. Source code is private and confidential.

© 2025 Valnox İnovasyon ve Reklam Promosyon A.Ş. All rights reserved.

---

<p align="center">
  <sub>Keywords: license plate recognition, LPR, ANPR, automatic number plate recognition, parking management, vehicle access control, YOLO, OCR, ONNX, DirectML, WinUI, .NET 8, Turkey, plaka tanıma, otopark yönetimi, araç erişim kontrolü</sub>
</p>
