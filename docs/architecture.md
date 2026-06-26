# System Architecture

TerraSense is designed with a hybrid edge-cloud architecture, prioritizing low-bandwidth environments while delivering advanced AI insights.

## Current Prototype Architecture
The current implementation is a zero-build React SPA prototype designed for rapid UI/UX validation.

* **Frontend**: React 18, Tailwind CSS, Lucide Icons
* **Data Flow**: Static simulation of telemetry data for UX testing.
* **Deployment**: Static hosting via GitHub Pages / Vercel.

## Future Production Architecture

### 1. Edge Node (Hardware)
* **Microcontroller**: ESP32 for low-power operation and deep sleep cycles.
* **Sensors**: Soil moisture (capacitive), Temperature/Humidity (DHT22 or similar), NPK sensors.
* **Connectivity**: GSM/GPRS module for remote data transmission in areas without WiFi.
* **Power**: Solar panel with Li-ion battery backup.

### 2. Cloud Backend
* **API Gateway**: FastAPI (Python) for handling high-frequency sensor data ingestion.
* **Database**: TimescaleDB / PostgreSQL for time-series telemetry data.
* **AI Engine**: Predictive models for crop yield and disease detection based on micro-climate data.

### 3. Voice Assistant
* **NLP**: Vernacular language support for farmers with low literacy.
* **Interface**: Twilio integration for SMS/Voice interactions and in-app voice commands.
