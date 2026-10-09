# ASRA - Silent Safety Band | IAC 2026 - V2.1 FINAL

> Autonomous 4G Wearable Safety Band with Multi-Stage Biometric Fall Verification & Dual Guardian FCM Alert

### 1. Problem Statement
- Women & children feel unsafe in transit; panic bands with loud sirens get snatched.
- Elderly falls have delayed response.
- Smartwatches cost >15k, need phone Bluetooth, battery dies in 24hrs.

### 2. Our Solution - V2.1
Standalone waterproof band (48x28mm, 4-Layer) that works without phone.
- Hardware: ESP32-S3-MINI-1U + SIM7080G NB-IoT/Cat-M + GNSS + MFF2 eSIM
- One-Press Silent SOS: Dome button -> Live Location via NB-IoT -> FCM Multicast to 2 guardians in <3 sec
- Two-Stage Fall Verification: MPU-6050 impact + MAX30102 heart-rate surge (98% false alarm cut)
- 3-Day Battery: PSM/eDRX deep sleep, wake only on MPU INT (GPIO5)

### 3. Technical Architecture
- MCU: ESP32-S3-MINI-1U
- Cellular: SIM7080G + U.FL LTE & GNSS Antennas
- Sensors: MPU-6050 (0x68), MAX30102 Bottom (0x57)
- Power: TP4054 -> SY8205A Buck 3.8V -> ME6211 LDO 3.3V
- Backend: Node.js + MQTT + MongoDB + FCM

### 4. Repository Structure
/hardware - Schematic PDF & 3D Render only
/firmware - SOS + PSM logic
/backend  - Node.js API + MQTT (Full code)
/app      - Guardian App

### 5. How to Run
cd backend
npm install
npm start

### 6. Team ASRA
Arpa Gupta - Hardware + Embedded + Backend

### 7. License
Proprietary - For IAC 2026 Evaluation Only. Gerber and firmware PSM algo are confidential IP.