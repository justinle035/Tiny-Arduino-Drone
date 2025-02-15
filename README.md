https://husteduvn-my.sharepoint.com/:p:/g/personal/nguyen_lbn233924_sis_hust_edu_vn/EVf5MJjW4dBNssF8ulI2DoEBOlme6Lq3PthxhSLgafDfcA

# Mini FPV Drone with Integrated Object Detection

## Overview
A cost-efficient mini FPV drone featuring real-time object detection and remote control. Built with custom PCB modules, Arduino-based firmware, and optimized performance through parameter calibration.

## Key Features
- **Modular Hardware Design**: PCB blocks (flight controller, ESC, Rx/Tx) designed in Altium.
- **Arduino Firmware**: Custom control logic for flight stability and command processing.
- **MultiWiiCfg Calibration**: Fine-tuned PID parameters for optimal flight dynamics.
- **Object Detection**: Onboard algorithm for obstacle identification (CV-based).
- **Remote Control**: Low-latency command transmission via radio modules.
- **Testing Framework**: Predefined scenarios for stress/performance evaluation.

## Technical Specifications
### Hardware
- **Frame**: 120mm mini quadcopter (3D-printed/carbon fiber)
- **Flight Controller**: ATmega328P (Arduino Nano-compatible)
- **FPV Camera**: 600TVL CMOS (5V, analog output)
- **Object Detection**: OV7670 camera + embedded algorithm
- **ESCs**: 4-in-1 12A BLHeli
- **Motors**: 1103 10000KV brushless
- **Battery**: 2S 450mAh LiPo
- **Radio**: FrSky D8 protocol (2.4GHz)

### Software
- **Firmware**: Arduino IDE (C/C++)
- **Communication Protocol**: PWM (ESCs), SPI/I2C (sensors)
- **Calibration**: MultiWiiCfg GUI
- **Object Detection**: Custom algorithm (TensorFlow Lite/OpenCV)
------------------------------------------------------------------------------

Compile/upload via Arduino IDE.

Calibration

Connect flight controller to MultiWiiCfg.

Adjust PID values for roll/pitch/yaw.

Testing

Execute scenarios: test_stability.py, test_object_detection.py.

Object Detection Setup

Flash detection algorithm to onboard processor.

Configure camera FOV in config.h.

Testing Scenarios
Flight Stability
Hover tests (indoor/outdoor) with varying wind conditions.

Object Detection Accuracy
Validate detection range (0.5m–3m) against moving targets.

Control Latency
Measure input-to-action delay via high-speed camera.

Battery Endurance
Full-throttle runtime assessment (2S/3S LiPo).
