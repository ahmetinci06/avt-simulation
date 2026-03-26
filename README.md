# ⚙️ AVT Racing — Malzeme & Simülasyon Ekibi

## 📊 İlerleme & Çalışma Akışı

- [🔄 WORKFLOW.md](WORKFLOW.md) — Çalışma akışı ve PR kuralları
- [📊 PROGRESS.md](PROGRESS.md) — Görev durumları ve ilerleme
- [🐛 BUGS.md](BUGS.md) — Bug raporları ve debug takibi

> Her değişiklik PR ile yapılır. Review: @ahmetinci06 & Yaver (AI CTO)

---



> **avt-simulation** — Simülasyon dosyaları, malzeme analizi, FEA sonuçları ve hesaplamalı dinamik akışkanlar simülasyonlarının deposu.

[![Ana Hub](https://img.shields.io/badge/Ana%20Hub-avt--hub--dev-blue)](https://github.com/ahmetinci06/avt-hub-dev)
[![TEKNOFEST 2026](https://img.shields.io/badge/TEKNOFEST-2026-red)](https://teknofest.org)

---

## 📋 Hakkında

Bu repo, AVT Racing aracının yapısal ve aerodinamik simülasyonlarını, malzeme seçim analizlerini ve FEA (Finite Element Analysis) sonuçlarını barındırır.

**Merkezi Hub:** [avt-hub-dev](https://github.com/ahmetinci06/avt-hub-dev)

---

## 👥 Malzeme & Simülasyon Ekibi

| İsim | Rol |
|------|-----|
| Ömer Arda Dündar | Malzeme & Simülasyon |
| Emre Göğer | Malzeme & Simülasyon |
| Serhad Agın | Malzeme & Simülasyon |

---

## 📁 Klasör Yapısı

```
avt-simulation/
├── fea/                        # Finite Element Analysis
│   ├── chassis/                # Şasi FEA
│   ├── suspension/             # Süspansiyon FEA
│   └── impact/                 # Darbe analizi
├── cfd/                        # Computational Fluid Dynamics
│   ├── aerodynamics/           # Aerodinamik analiz
│   └── thermal/                # Termal analiz
├── materials/                  # Malzeme analizi ve seçimi
│   ├── database/               # Malzeme özellikleri
│   └── selection-reports/      # Malzeme seçim raporları
├── dynamics/                   # Araç dinamiği simülasyonları
│   ├── lap-simulation/         # Tur simülasyonu
│   └── suspension-kinematics/  # Süspansiyon kinematiği
├── scripts/                    # Python/MATLAB analiz scriptleri
├── results/                    # Analiz sonuçları (özet, grafik)
│   ├── reports/                # PDF raporlar
│   └── plots/                  # Grafikler ve görseller
├── references/                 # Referans makaleler, standartlar
└── docs/
    ├── GITHUB-GUIDE.md
    └── simulation-methodology.md
```

---

## 🔧 Kullanılan Yazılımlar

| Yazılım | Alan | Format |
|---------|------|--------|
| ANSYS | FEA, CFD | `.wbpz`, `.cas` |
| SolidWorks Simulation | FEA | `.SLDPRT` |
| MATLAB/Simulink | Sistem simülasyonu | `.m`, `.slx` |
| Python (NumPy, SciPy) | Hesaplama | `.py`, `.ipynb` |
| OpenFOAM | CFD (açık kaynak) | Klasör yapısı |
| ADAMS | Çok gövde dinamiği | `.cmd`, `.bin` |

---

## 🌿 Branch Yapısı

```
main          ← Onaylanmış, final simülasyon sonuçları
  └── develop ← Aktif analizler
        ├── sim/chassis-fea-v2
        ├── sim/aerodinamik-cfd
        └── analysis/malzeme-secimi
```

### Branch İsimlendirme
```
sim/<analiz-tipi>-<bileşen>     # Simülasyon
analysis/<konu>                  # Analiz raporu
fix/<analiz>-revize             # Düzeltme
```

---

## 📊 Sonuç Dosyası Kuralları

- **Büyük simülasyon sonuç dosyaları** (>.result, .cas): Google Drive'a yükle
- **Özet raporlar** (PDF): `results/reports/` klasörüne ekle
- **Grafikler ve görseller**: `results/plots/` klasörüne ekle
- **Python/MATLAB scriptleri**: `scripts/` klasörüne ekle
- Her analiz için `results/reports/` klasörüne kısa bir özet raporu (Markdown veya PDF) ekle

---

## 🐍 Python Scripti Kullanımı

```bash
# Sanal ortam oluştur
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Bağımlılıkları yükle
pip install -r requirements.txt

# Analiz scriptini çalıştır
python scripts/fea_post_process.py
```

---

## 🚀 Hızlı Başlangıç

```bash
git clone git@github.com:ahmetinci06/avt-simulation.git
cd avt-simulation
git checkout develop
git checkout -b sim/yaptığın-analiz
```

Detaylı rehber: [docs/GITHUB-GUIDE.md](docs/GITHUB-GUIDE.md)

---

## 📚 Kaynaklar

- [CONTRIBUTING.md](CONTRIBUTING.md)
- [docs/GITHUB-GUIDE.md](docs/GITHUB-GUIDE.md)
- [Ana Hub — avt-hub-dev](https://github.com/ahmetinci06/avt-hub-dev)

---

*🏎️ AVT Racing — TEKNOFEST 2026 | Malzeme & Simülasyon Ekibi*