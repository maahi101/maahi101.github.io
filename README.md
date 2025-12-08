# maahi101.github.io
Smart People's Smart Project😎

Team Name: Smart(People)
Team Members:

🙋🏻‍♂️Rajath Ramana (rajath@seas.upenn.edu)

🙋🏻‍♀️Maahi Trivedi (maahit1@seas.upenn.edu)

🙋🏻‍♂️Vihaan Ravishankar (vihaan1@seas.upenn.edu)

🎯 Abstract

This project, GAIA (Gait-based Authentication and Identity Assistant), introduces a novel approach to biometric authentication through gait analysis integrated into smart footwear. Unlike conventional biometrics such as fingerprints or facial recognition, gait provides a continuous, unobtrusive, and behaviorally unique means of identifying individuals.
The proposed system embeds inertial and pressure sensors within a shoe to capture real-time gait data, which is transmitted via Bluetooth to a mobile device for analysis. A machine learning model processes this data to generate a distinct gait signature for each user, enabling secure and contactless authentication.
GAIA demonstrates the convergence of wearable technology, embedded sensing, and AI-based biometrics, paving the way for intelligent, user-friendly, and non-invasive identity verification systems applicable in security, healthcare, and personalized IoT environments.

💡 Motivation

As digital systems become increasingly integrated into daily life, the demand for secure yet seamless authentication methods continues to rise. Conventional biometrics—such as fingerprints, facial recognition, or iris scans—while effective, often require direct user interaction, can be spoofed through replicas or images, and may fail under adverse conditions like poor lighting or physical obstructions.

Why Gait?🤔
Gait offers a compelling alternative as a biometric trait:

Unique: Every individual has a distinct walking pattern influenced by their physiology, posture, and muscle coordination
Non-invasive: Can be captured passively without interrupting user activity
Difficult to forge: Remains challenging to imitate or replicate
Continuous: Provides ongoing authentication during natural movement

The motivation behind GAIA is to harness this uniqueness of gait for continuous, contactless authentication through an intelligent wearable system. By embedding motion and pressure sensors within a shoe, GAIA aims to establish a new paradigm of authentication—one that is natural, secure, and integrated seamlessly into daily human motion.

🛠️Critical Components

<img width="623" height="348" alt="image" src="https://github.com/user-attachments/assets/beeb1a46-45fe-4c73-b981-a9538bf525f2" />

✨ Key Features
1. Hardware

Custom bare-metal firmware - Written entirely in C without Arduino libraries
Software-implemented I²C - Bit-banged protocol for IMU communication
Software-implemented SPI - Manual bit-toggling for BLE SDEP packets
Real-time sensor fusion - Synchronized IMU and pressure data acquisition
Low-power design - 8+ hour operation on single battery charge
Compact wearable form factor - Electronics integrated into shoe insole

2. Software

Custom device drivers for I²C, SPI, ADC, and IMU
Real-time gait data streaming via Bluetooth Low Energy
Machine learning pipeline for gait analysis and authentication
Step detection algorithm using pressure transitions and accelerometer peaks
Feature extraction - Cadence, step time, pressure symmetry
Identity recognition using trained ML models
Fall detection capability

3. Data Processing

Packet format: FLEX,AX,AY,AZ,GX,GY,GZ
Transmission rate: 3-4 Hz
Sensor synchronization: ±5 ms accuracy
Step detection accuracy: ≥90%
Authentication accuracy: ≥85% (offline testing)

🚀 Future Work
Potential Enhancements:

1. Dual-shoe system for bilateral gait comparison
2. On-device authentication with thresholded matching
3. OLED display for real-time feedback
4. Data logging to onboard EEPROM or external flash
5. Enhanced ML models with larger training datasets
6. Mobile app with comprehensive UI
7. Web portal for user management and analytics
8. Additional sensors for temperature and heart rate
9. Improved enclosure with waterproofing

Research Directions:

1. Multi-user household authentication
2. Gait-based health monitoring (fall risk, mobility assessment)
3. Integration with smart home and IoT ecosystems
4. Continuous authentication for secure facilities
5. Rehabilitation and physical therapy applications

🏆 Accomplishments
What We're Proud Of

1. Bare-metal firmware implementation without relying on Arduino libraries
2. Custom protocol implementations for I²C and SPI from scratch
3. Real-time embedded system achieving sub-millisecond timing accuracy
4. Successful sensor fusion combining IMU and pressure data
5. Working ML pipeline for gait-based authentication
6. Wearable integration maintaining comfort and functionality
