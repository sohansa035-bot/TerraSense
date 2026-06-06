# Terra Sense: Phygital AgTech 🌾☀️

> **Solar-powered voice AI hardware that empowers smallholder farmers with vernacular climate advisory and tracking.**

Terra Sense is an enterprise-grade prototype designed for the "Ignite Venture Milestone 3" project. It addresses the massive ₹92,000 Cr. annual post-harvest loss in India by providing farmers with a "Ground-Truth" Edge Computing solution: actionable, hyper-local farming prescriptions delivered via a zero-UI, solar-powered voice assistant.

## 🚀 The Digital Prototype
Currently, the repository contains the digital "Software" and "Sales" presentation components of the Terra Sense ecosystem:

1. **The Marketing Landing Page (`index.html`)**
   - A highly professional, "bento-box" style GTM website.
   - Highlights the ₹2,500 transparent pricing model, Unit Economics, and Go-To-Market strategy.
   - Includes a lead generation CRM simulation for Farmer Producer Organizations (FPOs).
   - *Tech Stack: HTML, Tailwind CSS, JavaScript (Intersection Observers).*

2. **The Predictive Analytics Dashboard (`agri.html`)**
   - A React-based "Mission Control" simulation of the farmer's interface.
   - **Ground Truth Telemetry:** Live dials for Soil Moisture, Micro-Climate, Vapor Pressure, and Nitrogen levels.
   - **Multispectral Overlay:** Simulated heatmap overlay of crop health.
   - **Prescription Logic:** AI-driven actionable insights (e.g., "Apply 5L Urea/Acre").
   - *Tech Stack: React.js (via CDN), Babel, Tailwind CSS, Lucide Icons.*

---

## 🛠️ Future Hardware Prototype (Roadmap)
The core Unique Value Proposition (UVP) of Terra Sense is **"Intelligence Without Internet"** via an autonomous physical node. The following is the engineering roadmap to transition this digital prototype into a physical hardware device.

### Required Components (BOM)
*   **Microcontroller:** ESP32-WROOM-32E (Built-in WiFi/Bluetooth, adequate processing for audio streams).
*   **Audio Input:** MAX9814 Electret Microphone Amplifier (for pristine vernacular voice capture).
*   **Audio Output:** I2S MAX98357A Audio Amplifier + 3W 4-Ohm Waterproof Speaker.
*   **Telemetry Sensors:**
    *   Capacitive Soil Moisture Sensor v1.2 (Corrosion resistant).
    *   BME280 (Temperature, Humidity, Barometric Pressure for Micro-climate).
    *   NPK Sensor (RS485 Modbus compatible) for soil nutrition.
*   **Connectivity:** SIM800L / SIM7600G (GSM/4G LTE Module for remote field syncing).
*   **Power System:** 5V 1A Mini Solar Panel + TP4056 Lipo Charger + 18650 Li-ion Battery (3000mAh).

### Firmware & Execution Strategy
1. **Edge Node Assembly:** 
   Connect the ESP32 to the MEMS microphone via ADC. The ESP32 acts as the core edge processor.
2. **Audio Wake Word (Zero-UI):** 
   Implement a lightweight wake-word engine (like *Picovoice Porcupine*) on the ESP32 so the farmer can just say "Hey Terra" in the field.
3. **Telemetry Polling:** 
   The ESP32 polls the Soil, BME280, and NPK sensors every 30 minutes, writing the data to local memory to conserve battery.
4. **Cloud Sync (Global Core):**
   When the farmer asks a question, the ESP32 uses the GSM module to send the audio payload and recent telemetry to the backend (Python/Node.js).
5. **AI Inference:**
   The backend uses an LLM (OpenAI / Gemini) coupled with the telemetry data to generate a vernacular text response, converts it to speech (TTS), and sends the audio file back down to the field node to be played over the speaker.

## 💻 How to Run
Because this prototype is entirely browser-based and uses CDNs, there are **no dependencies or build steps** required.
1. Clone this repository.
2. Double-click `index.html` to view the Investor/FPO Pitch.
3. Double-click `agri.html` to interact with the Dashboard Simulation.

---
*Developed for the Venture Viability Project | Reva University © 2026*
