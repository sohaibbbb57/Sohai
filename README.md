# 🤖 AgentHub

**AgentHub**, Android cihazlar üzerinde çalışan, ekranı analiz edebilen ve erişilebilirlik (accessibility) servislerini kullanarak otonom görevler gerçekleştirebilen **on-device LLM AI Agent** altyapısıdır. 

OpenAI, Claude veya yerel (local) LLM sağlayıcılarını cihaz üzeri otomasyonla birleştirerek Android arayüzü üzerinde insan gibi tıklama, kaydırma ve veri işleme görevlerini yürütür.

---

## 🚀 Özellikler

* **On-Device Brain Bridge:** Farklı LLM sağlayıcılarını (OpenAI, Claude, Ollama vb.) modüler şekilde bağlama imkanı.
* **Autonomous Screen Processing:** `MediaProjection` ve `AccessibilityService` entegrasyonu sayesinde ekranı anlık analiz etme ve dinamik tıklama/kaydırma eylemleri gerçekleştirme.
* **Foreground Service:** Android bellek yönetiminden etkilenmeden arka planda kesintisiz çalışan ajan altyapısı.
* **Tool Registry Architecture:** Ajana yeni yetenekler (araçlar) eklemeyi kolaylaştıran esnek mimari.
* **Automated CI/CD:** GitHub Actions üzerinden her `push` işleminde otomatik derlenen ve APK çıktısı veren pipeline.

---

## 🏗️ Proje Mimarisi

```text
AgentHub/
├── app/src/main/java/com/devran/agenthub/
│   ├── agent/             # Agent Engine, Tool Registry & Prompts
│   ├── automation/        # Accessibility & Foreground Services
│   ├── bridge/            # Provider Bridge (LLM Integrations)
│   ├── data/              # Config & Agent State Store
│   ├── screen/            # MediaProjection Screen Capture
│   └── util/              # Runtime Checks & Validations
├── docs/                  # Mimari ve modül dokümantasyonları
├── scripts/               # Preflight ve derleme kontrol betikleri
└── .github/workflows/     # CI/CD Otomatik APK build akışı

