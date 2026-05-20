<p align="center">
  <img src="logo-2400.png" alt="Plakanet Logo" width="180" />
</p>

<h1 align="center">Plakanet</h1>

<p align="center">
  Yapay zeka destekli plaka tanıma ve araç erişim yönetim sistemi
</p>

<p align="center">
  <a href="https://plakanet.net">🌐 Web Sitesi</a> •
  <a href="https://plakanet.net/tr/pricing">💰 Fiyatlandırma</a> •
  <a href="https://plakanet.net/tr/faq">❓ SSS</a> •
  <a href="https://apps.microsoft.com/detail/Plakanet">📦 Microsoft Store</a>
</p>

---

## Nedir?

**Plakanet**, küçük işletmeler, siteler ve otoparklar için geliştirilmiş yapay zeka tabanlı plaka tanıma (LPR/ANPR) sistemidir. IP veya USB kameralar üzerinden gerçek zamanlı plaka algılama, araç erişim kontrolü ve raporlama sunar.

## Özellikler

| Özellik | Açıklama |
|---------|----------|
| 🤖 **AI Plaka Tanıma** | ONNX tabanlı derin öğrenme modeli ile yüksek doğrulukta plaka algılama ve OCR |
| 🏢 **Site Modu** | Yetkili araç listesi, giriş/çıkış kaydı, yetkisiz araç uyarısı |
| 🅿️ **Otopark Modu** | Otomatik süre hesaplama, ücretlendirme, doluluk takibi |
| 📷 **Çoklu Kamera** | Sınırsız IP kamera (RTSP) ve USB webcam desteği |
| ⚡ **Gerçek Zamanlı** | Kayıpsız görüntü pipeline, kamera başına ayarlanabilir FPS |
| 📊 **Raporlar** | Günlük/aylık erişim logları, gelir özetleri, Excel dışa aktarım |
| 🔑 **Lisanslama** | 7 günlük ücretsiz deneme, aylık/yıllık abonelik |
| 🌐 **Web Portal** | Lisans yönetimi, kullanıcı paneli — [plakanet.net](https://plakanet.net) |
| 💻 **Windows Native** | WinUI 3 + .NET 8, MSIX paketleme, Microsoft Store dağıtımı |
| 🎯 **DirectML GPU** | NVIDIA/AMD/Intel GPU hızlandırma (DirectML üzerinden) |

## Ekran Görüntüleri

<p align="center">
  <img src="admin-dashboard-v2.png" alt="Dashboard" width="700" />
</p>

## Başlarken

### Gereksinimler

- Windows 10 sürüm 1903 veya üzeri (x64)
- RTSP uyumlu IP kamera veya USB webcam
- NVIDIA/AMD GPU önerilir (DirectML desteği)

### Kurulum

1. [Microsoft Store](https://apps.microsoft.com/detail/Plakanet)'dan indirin veya [plakanet.net](https://plakanet.net) üzerinden edinin
2. Uygulamayı açın → Lisans ekranında "Ücretsiz Lisans Al" ile [plakanet.net](https://plakanet.net/app/licenses) üzerinden 7 günlük deneme alın
3. Kurulum sihirbazı ile mod seçimi (Site/Otopark) ve kamera yapılandırması yapın
4. Sistemi başlatın

## Mimari

```
┌─────────────────────────────────────────────┐
│  WPF Masaüstü Uygulaması (WinUI 3 / .NET 8) │
│  ├── Kamera Servisi (RTSP TCP / USB)         │
│  ├── AI Engine (ONNX DirectML)               │
│  ├── SQLite Veritabanı                       │
│  └── Lisans Yönetimi                         │
└──────────────────┬──────────────────────────┘
                   │ HTTPS
┌──────────────────▼──────────────────────────┐
│  Web Backend (Next.js / Node.js)             │
│  ├── Firebase Auth                           │
│  ├── Lisans API                              │
│  ├── Admin Panel                             │
│  └── Landing Page (plakanet.net)             │
└─────────────────────────────────────────────┘
```

## Teknoloji Yığını

**Masaüstü:** .NET 8, WinUI 3, OpenCvSharp, ONNX Runtime (DirectML), Entity Framework Core, SQLite

**Web:** Next.js 16, TypeScript, Tailwind CSS, Firebase Auth, SQLite (better-sqlite3)

**Altyapı:** Docker, Caddy, GitHub Actions CI/CD

## Fiyatlandırma

| Plan | Fiyat | Süre |
|------|-------|------|
| Deneme | Ücretsiz | 7 gün |
| 6 Aylık | $199 | 6 ay |
| Yıllık | $349 | 12 ay |

Detaylar için: [plakanet.net/pricing](https://plakanet.net/tr/pricing)

## Lisans

Bu yazılım tescilli bir üründür. Kaynak kodu özel ve gizlidir.

© 2025 Valnox İnovasyon ve Reklam Promosyon A.Ş. Tüm hakları saklıdır.

## İletişim

- 🌐 [plakanet.net](https://plakanet.net)
- 📧 info@plakanet.net
