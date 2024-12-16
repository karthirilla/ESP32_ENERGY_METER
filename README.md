# ESP32 Energy Meter for Agriculture Automation

## Overview
The **ESP32 Energy Meter for Agriculture Automation** is a versatile, IoT-enabled embedded system designed for precision energy monitoring and seamless integration into agricultural environments. Built on the powerful **ESP32-S3 microcontroller**, this project combines wide-range power capabilities, isolated communication, and advanced peripherals to enhance automation, data management, and control for modern agriculture.

![Front View](https://github.com/karthirilla/ESP32_ENERGY_METER/blob/main/ESP32_Energy_Meter_Front_Black.png)
![Back View](https://github.com/karthirilla/ESP32_ENERGY_METER/blob/main/ESP32_Energy_Meter_Back_Black.png)

# ESP32 Energy Meter

## View Images

| **Image 1**                           | **Image 2**                           | **Image 3**                           |
|----------------------------------------|----------------------------------------|----------------------------------------|
| ![Front 1](https://github.com/karthirilla/ESP32_ENERGY_METER/blob/main/ESP32_Energy_Meter_Front_1.jpg) | ![Front 2](https://github.com/karthirilla/ESP32_ENERGY_METER/blob/main/ESP32_Energy_Meter_Front_2.jpg) | ![Front 3](https://github.com/karthirilla/ESP32_ENERGY_METER/blob/main/ESP32_Energy_Meter_Front_3.jpg) |

---

## Key Features

### 1. **Wide-Range Power Supply**
- Supports input voltages up to **40V**.
- Includes an **isolated step-down converter** to minimize power supply noise and ensure stable operation even in noisy environments.

### 2. **Microcontroller**
- Powered by the **ESP32-S3**, featuring:
  - Dual-core processor.
  - WiFi and BLE (Bluetooth Low Energy) support for wireless connectivity.
  - Ample GPIOs and extended peripherals.

### 3. **External Peripherals**
- **RTC (DS3231)**: High-precision real-time clock for time-critical operations.
- **EEPROM**: Stores data locally for retaining critical information during power outages.
- **I2C IO Extender**: Expands GPIO outputs to support more sensors, relays, and modules.

### 4. **Communication Interfaces**
- **LoRa Module**: Long-range, low-power wireless communication for transmitting data over large distances.
- **WiFi & BLE**: Seamless short-range communication for cloud integration or app-based control.
- **RS232 and RS485**: Industrial-grade communication protocols for connecting sensors, PLCs, and other devices.
- Support for **external extension modules** to add further connectivity options.

### 5. **Display and Control**
- **3.5-inch LCD Display**: High-resolution, large display for showcasing real-time data and analytics.
- **4 Input Buttons**: Intuitive control interface for navigation and input.

### 6. **I/O Management**
- Multiple **isolated inputs and outputs** for safe and reliable operation in harsh environments.
- Scalable I/O system through the **I2C IO Extender**.

---

## System Architecture

### Hardware Components
| Component                | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| ESP32-S3 Microcontroller | Core processing unit with WiFi, BLE, and dual-core architecture.            |
| DS3231 RTC               | Ensures accurate timekeeping for scheduled operations.                     |
| EEPROM                   | Stores configuration and data locally during power loss.                   |
| I2C IO Extender          | Expands the GPIO capabilities for additional devices.                      |
| Isolated Step-Down Converter | Converts power supply to regulated voltage while minimizing noise.       |
| LoRa Module              | Provides long-range wireless communication.                                |
| RS232/RS485              | Industrial communication interfaces for reliable device connectivity.      |
| LCD Display (3.5-inch)   | Displays real-time data, parameters, and system status.                    |
| Input Buttons            | Facilitates user interaction and system control.                           |

### Communication Overview
| Communication Protocol | Purpose                                                                     |
|-------------------------|-----------------------------------------------------------------------------|
| WiFi                   | Cloud connectivity and real-time monitoring via web or app.               |
| BLE                    | Short-range communication with mobile devices or BLE-enabled sensors.      |
| LoRa                   | Long-range communication for remote locations.                            |
| RS232/RS485            | Integrates with industrial equipment and external modules.                 |

---

## Use Cases

1. **Energy Monitoring in Agriculture**
   - Monitor and control energy consumption for agricultural equipment, pumps, and irrigation systems.
   - Reduce energy wastage by analyzing real-time data on the LCD display.

2. **Automation and Scheduling**
   - Use the RTC (DS3231) to schedule operations like irrigation, lighting, or motor control.
   - Store and retrieve operational data using the EEPROM.

3. **Remote Monitoring**
   - Leverage LoRa for data transmission across large farmlands.
   - Access real-time metrics using WiFi or BLE via mobile apps or cloud dashboards.

4. **Industrial Integration**
   - Use RS232 and RS485 interfaces to connect with sensors, PLCs, and external devices for process control.

5. **User-Friendly Operation**
   - View detailed system stats on the 3.5-inch LCD.
   - Utilize input buttons for on-device configuration without the need for external tools.

---

## Technical Specifications

### Microcontroller
| Parameter                  | Value                                  |
|----------------------------|----------------------------------------|
| Model                     | ESP32-S3                              |
| WiFi/BLE Support           | 802.11b/g/n, Bluetooth v5.0 LE        |
| GPIO Pins                  | Multiple (expandable with I2C Extender) |

### Power Supply
| Parameter                  | Value                                  |
|----------------------------|----------------------------------------|
| Input Voltage Range        | 5V to 40V                             |
| Step-Down Converter        | Isolated, noise-resistant              |

### Communication
| Interface                 | Specification                          |
|---------------------------|----------------------------------------|
| WiFi                      | 2.4GHz                                 |
| BLE                       | Bluetooth v5.0 LE                     |
| LoRa                      | Long-range, low-power communication    |
| RS232/RS485               | Standard industrial interfaces         |

### Display and Controls
| Parameter                 | Value                                  |
|---------------------------|----------------------------------------|
| Display                   | 3.5-inch LCD                          |
| Buttons                   | 4 (input buttons for navigation)       |

---

## Getting Started

### Prerequisites
- **Hardware**: ESP32-S3 Development Board, RTC DS3231 module, I2C IO Extender, LoRa Module, and supporting peripherals.
- **Software**: Arduino IDE (with ESP32 support) or PlatformIO.

### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/esp32-energy-meter.git
   ```
2. Install the necessary libraries in your Arduino IDE:
   - `WiFi.h`
   - `Wire.h`
   - `EEPROM.h`
   - `RTClib.h`
   - `LoRa.h`
3. Connect the components as per the circuit diagram (provided in the repository).
4. Compile and upload the code to your ESP32-S3.

---

## Circuit Diagram
[Click here](link-to-circuit-diagram) to view the circuit diagram.

---

## Code Overview
The code includes the following key functionalities:

- **Power Monitoring**: Interfaces with ADC pins to measure power metrics.
- **RTC Integration**: Uses the DS3231 module to maintain precise timing.
- **Data Storage**: Leverages EEPROM to store energy usage logs.
- **I2C Management**: Communicates with I2C-based IO extenders and peripherals.
- **LoRa Communication**: Transmits critical data wirelessly over long distances.
- **LCD Display**: Updates real-time stats for user reference.

---

## Future Enhancements
- Add support for MQTT to integrate with cloud platforms like AWS IoT or Firebase.
- Implement a mobile app for BLE-based real-time monitoring and control.
- Expand I/O capabilities to support additional sensors and actuators.
- Introduce over-the-air (OTA) firmware updates for easier maintenance.

---

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgments
- **ESP32 Community**: For continuous support and development.
- **Open-Source Libraries**: Used in this project for enhanced functionality.

---

## Contact
For any inquiries, feedback, or collaboration opportunities, feel free to reach out:
- **Email**: karthikrilla@gmail.com
- **LinkedIn**: [Karthi C](https://www.linkedin.com/in/jigar-sable/)

