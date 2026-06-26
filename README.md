<div align="center">

# 🌿 TerraSense

**Intelligence for Smallholder Farmers**

*From data to actionable farming decisions.*

**Founder & Product Engineer • Prototype • System Architecture**

</div>

---

## 🎯 Product Vision

Smallholder farmers operate on razor-thin margins and often rely on fragmented information, delayed weather updates, and manual decision-making. Extreme weather volatility, pests, and soil degradation reduce yields and income, resulting in massive post-harvest losses.

TerraSense is a scalable, low-cost AgTech product designed to transform environmental data into practical recommendations. By taking the guesswork out of farming, we provide clear, actionable insights when it matters most.

---

## 📊 Market Validation & Competitive Analysis

### The Market Gap
* **$20B+ TAM**: According to industry reports, the precision agriculture market is booming, but current solutions target massive commercial farms. [See sources in `docs/market-research.md`]
* **The Missing 30%**: Smallholder farmers produce 30% of the world's food but are entirely priced out of existing AgTech solutions.

### Competitive Positioning

| Feature | Existing Solutions | TerraSense |
| :--- | :--- | :--- |
| **Language** | English only | Local / Vernacular |
| **Connectivity** | High-speed Internet required | Offline-first / GSM Edge Node |
| **Interface** | Complex Mobile/Web UI | Voice Assistant First |
| **Hardware** | $1,000+ proprietary rigs | Planned Low-cost ESP32 Edge Node |

---

## 🗺️ The Product Journey

TerraSense creates a closed-loop system for farm management:

**Observe** ➔ **Collect** ➔ **Analyze** ➔ **Recommend** ➔ **Act**

### Core User Story

> **Farmer notices yellow leaves** ➔ **Asks TerraSense** ➔ **Receives diagnosis** ➔ **Gets fertilizer recommendation** ➔ **Improves yield**

---

## 📸 Product Screens (Prototype)

<div align="center">
  <img src="assets/dashboard.png" alt="Mission Control Dashboard Prototype" width="90%" />
</div>

*Planned Product Screens:*
- ✅ **Dashboard** (Shown above)
- ⏳ **Farmer Home**
- ⏳ **Ask Assistant**
- ⏳ **Alerts**
- ⏳ **Crop Health**
- ⏳ **Weather**

---

## 🚀 Product Roadmap

Investors and stakeholders can track our development milestones here:

| Phase | Milestone | Status |
| :--- | :--- | :--- |
| **v0.1** | Dashboard & UI/UX Prototype Validation | ✅ Complete |
| **v0.2** | Software Intelligence & Voice Assistant NLP | ⏳ In Progress |
| **v0.5** | Hardware Node Prototype Assembly | ⏳ Planned |
| **v1.0** | Pilot Testing (10-20 field nodes) | ⏳ Planned |
| **v2.0** | Commercial Deployment & B2B Integration | ⏳ Planned |

---

## ⚙️ System Architecture

### Current Implementation (Software Prototype)

The current repository houses the v0.1 UI/UX prototype, built as an HTML prototype enhanced with lightweight React components via CDN to allow instant deployment and rapid iteration without complex toolchains.

```mermaid
graph LR
    Farmer((Farmer))
    Dash[Mission Control Dashboard]
    Engine[Rule-based Recommendation Prototype]
    Recs[Actionable Recommendations]

    Farmer -->|Views| Dash
    Dash -->|Requests| Engine
    Engine -->|Generates| Recs
    Recs -->|Displayed to| Farmer
```

### Planned Edge Architecture (v0.5)

```mermaid
graph LR
    Sensors[On-field Sensors]
    ESP[ESP32 Microcontroller]
    GSM[GSM Wi-Fi Module]
    Cloud[Cloud AI Backend]
    Voice[Voice Assistant Interface]
    Farmer((Farmer))

    Sensors -->|Data| ESP
    ESP -->|Telemetry| GSM
    GSM -->|Network| Cloud
    Cloud -->|Response| Voice
    Voice -->|Audio| Farmer
```

---

## ⚖️ Engineering Decisions

* **Why Software First?**
  Validate product-market fit before investing heavily in hardware manufacturing.
* **Why Voice Interface?**
  Lowers the digital literacy barrier, allows hands-free usage, and provides immediate regional language support.
* **Why ESP32?**
  Low cost, extremely low power consumption (deep sleep), and highly documented for easy deployment.
* **Why GSM?**
  Provides significantly better and more reliable rural farm coverage than Wi-Fi or LoRaWAN.

---

## 🚧 Current Limitations

* **Prototype UI only**: The dashboard uses simulated static data for UX validation.
* **No hardware implementation yet**: Sensor nodes exist only in architectural planning.
* **Rule-based recommendation engine**: Predictive insights do not yet use live Machine Learning models.
* **Field validation pending**: True accuracy will be determined during v1.0 pilot testing.

---

## 📁 Repository Structure

We have adopted a product-centric repository structure, separating documentation, core prototypes, and static assets.

```text
TerraSense/
├── assets/         # Product screenshots, diagrams, and map textures
├── docs/           # Comprehensive Startup Documentation
│   ├── architecture.md
│   ├── business-model.md
│   ├── market-research.md
│   └── future-roadmap.md
├── prototype/      # React/HTML UI Prototypes
│   ├── index.html  # Product Pitch & Landing Page
│   └── agri.html   # Mission Control Dashboard Simulation
├── README.md       
└── LICENSE         
```

*For an in-depth dive into our business strategy, please explore the `docs/` folder.*

---

## 🛠 Hardware Status

TerraSense is adopting a **Software-First Validation** approach. While currently a digital prototype, the planned hardware edge node will utilize the following stack (implementation planned in v0.5):

| Component | Specification (Planned) |
| :--- | :--- |
| **Microcontroller** | ESP32 DevKit V1 |
| **Sensors** | Capacitive Soil Moisture, DHT22 Temp/Humidity |
| **Power** | 5V Solar Panel + Li-ion Battery |
| **Communication** | GSM Module |

---

## 💻 Installation & Usage

To view the v0.1 React Prototype:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/sohansa035-bot/TerraSense.git
   cd TerraSense/prototype
   ```
2. **Launch Local Server**:
   ```bash
   python -m http.server
   ```
   *(Or open using Live Server in VS Code)*
3. **View Pitch**: Open `http://localhost:8000/index.html`
4. **View Dashboard**: Open `http://localhost:8000/agri.html`

---

## 📄 License

This project is licensed under the MIT License.
