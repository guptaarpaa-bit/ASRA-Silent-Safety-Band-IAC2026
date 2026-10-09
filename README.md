# ASRA-Silent-Safety-Band-IAC2026
Autonomous 4G Wearable Safety Band with Multi-Stage Biometric Fall Verification &amp; Dual Guardian FCM Alert System
# ASRA - Silent AI Safety Band
> Autonomous Wearable Safety Band for Women, Children, Elders & Accident Detection

## Problem Statement
- **Women & Children Safety:** 42% of women feel unsafe in transit after dark; existing panic bands use loud sirens that are immediately stripped off by assailants.
- **Elderly Fall Vulnerability:** Over 53% of seniors face annual fall hazards, often leading to delayed medical response.
- **Smartwatch Limitations:** Conventional smartwatches cost ₹15,000+, require active phone Bluetooth tethering, and drain battery in 24 hours.

## Solution Overview
A standalone ₹3,499 wearable band (BOM approx ₹2,300) powered by ESP32-S3 and Quectel EC200U 4G LTE/GNSS:
- **Zero-Buzzer Silent Alerts:** Dual haptic confirmations with discrete alert dispatch.
- **Anti-Tamper Wrist Sense:** Optical IR sensing (MAX30102) triggers instant offline/online tamper alert if band is forcibly removed.
- **Two-Stage Fall Verification:** Combines kinetic impact profiling with post-fall struggle and autonomic heart-rate surge check (reduces 98% of false alarms).
- **Dual Guardian Multicast:** Instant push alert dispatch to Mom and Dad simultaneously via FCM multicast with Google Maps tracking.

## Technical Architecture
- **MCU:** ESP32-S3-MINI-1U (Hardware eFuse ID serialization, Ultra-low-power Deep Sleep)
- **Cellular & GNSS:** Quectel EC200U-CN LTE Cat-1 + Embedded GNSS
- **Sensors:** MPU-6050 (Kinetic/Impact 0x68), MAX30102 (Optical Biometric 0x57)
- **Backend Infrastructure:** Node.js, MQTT Broker, Firebase Firestore, Firebase Cloud Messaging (FCM)

## Repository Structure
