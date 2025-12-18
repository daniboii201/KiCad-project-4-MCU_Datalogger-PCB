# KiCad project #4: MCU Datalogger PCB
This is my fourth PCB design created using KiCad. Unlike my previous projects, this design focuses on building a microcontroller-based datalogger circuit. The board is intended for logging sensor data to external storage, making it useful for IoT and embedded applications. This project includes two PCB versions: a 2-layer design for cost efficiency and a 4-layer design for improved signal integrity and compact routing.

<img width="2000" height="1079" alt="image" src="https://github.com/user-attachments/assets/80e05733-5a3d-450f-8224-4595400b3a44" />

<img width="2000" height="1079" alt="image" src="https://github.com/user-attachments/assets/cafaf0de-91a3-4d7e-a956-fdb13b958425" />

<img width="2000" height="1047" alt="image" src="https://github.com/user-attachments/assets/1444f91a-627e-4f58-a14c-2f64ccf1134d" />

<img width="718" height="781" alt="image" src="https://github.com/user-attachments/assets/171e0a9a-0af5-4bb7-86f5-cdd1df64f26c" />

## Features
• Microcontroller-based datalogger for sensor data acquisition

• Support for external storage (microSD card interface)

• Power regulation for stable MCU operation

• Two PCB versions: 2-layer (budget-friendly) and 4-layer (optimized for EMI and routing)

• Designed for low-power applications and modular sensor connectivity

### Components
• Microcontroller: ATmega328P-AU

• EEPROM: 2 × 24LC2025

• Real-Time Clock: DS1337S_T_R

• Oscillators:
  – 32.768 kHz (RTC timing)

  – 16 MHz (MCU clock)

• Capacitors:
  – 2 × 22 pF
  
  – 2 × 0.1 µF
  
  – 1 × 100 nF
  
• Resistors:
  – 3 x 10 kΩ
  
  – 2 x 4.7 kΩ
  
  – 2 x 330 Ω
  
• LEDs: 2 for status indication

• Battery: For RTC backup

• Pin headers: For programming and sensor interfaces

### Characteristics:

### How It Works:
The MCU Datalogger PCB is designed to collect sensor data, process it, and store it reliably. Here’s the workflow:

1. Power Management

The board includes a voltage regulator that converts the input supply (battery or external source) to a stable 3.3 V or 5 V rail for the microcontroller and peripherals. Decoupling capacitors near the MCU and SD card ensure clean power and reduce noise.

2. Data Acquisition

Sensors connect via standard interfaces such as I²C, SPI, or UART. The microcontroller periodically reads sensor values based on programmed intervals or triggers.

3. Data Logging

The MCU writes the collected data to a microSD card using the SPI protocol. This allows large storage capacity and easy data retrieval for analysis.

4. Clock & Timing

A crystal oscillator provides accurate timing for logging intervals and communication protocols, ensuring data consistency.

5. PCB Layer Benefits

• 2-layer version: Simple and cost-effective, suitable for basic applications.

• 4-layer version: Includes dedicated ground and power planes for better signal integrity, reduced EMI, and improved reliability in noisy environments.
