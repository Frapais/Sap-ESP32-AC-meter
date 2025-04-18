# 🌿 Sprig Labs – Sap AC Measurement Expansion Board

**Sap** is a compact and modular **AC current measurement expansion board** designed for non-invasive power monitoring in smart home and IoT applications. It is part of the **SprigStack ecosystem**, a collection of modular, stackable PCBs centered around the **Sprig ESP32-C3 Development Board**.

## 🔌 What It Does

Sap allows you to measure real-time AC current consumption from household or industrial appliances using a **Current Transformer (CT) sensor**—such as the SCT-013—without any direct connection to high-voltage wiring. It's ideal for use cases like:

- Smart home power monitoring
- Energy-aware automation triggers
- Real-time usage analytics

---

## 🧩 Features

- 📏 **Non-invasive AC current sensing**
- ⚡ Works with **CT sensors** (e.g., SCT-013)
- 🧠 **Designed for ESPHome** & **Home Assistant**
- 🔗 Seamlessly integrates with the **SprigStack modular ecosystem**
- 🪛 3.5mm female jack input for CT sensor
- 🔌 Analog output signal for ESP32-C3 ADC

---

## 🛠️ Hardware Overview

- **Input:** CT sensor via 3.5mm jack
- **Output:** Scaled analog signal for ESP32 ADC
- **Power Supply:** 3.3V (from Sprig board or external regulator)
- **Form Factor:** Stackable and compact, designed to work with other Sprig expansion boards

---

## 🧪 ESPHome Configuration Example

Below is a basic example of how to integrate Sap into your ESPHome YAML configuration using the ESP32 ADC:

```yaml
sensor:
  - platform: adc
    pin: GPIO3
    name: "AC Current Sensor"
    update_interval: 10s
    filters:
      - multiply: 30.0  # Adjust based on your CT sensor and resistor values
    unit_of_measurement: "A"
```

> ⚠️ Note: The `multiply` factor depends on the specific CT sensor and burden resistor used. Calibration may be necessary.


## 🧰 Getting Started

1. Solder your CT sensor to the screw terminal.
2. Connect Sap to the Sprig ESP32-C3 board or your preferred microcontroller.
3. Upload the ESPHome config to your device.
4. View real-time current readings in Home Assistant or any ESPHome dashboard.

---

## 💡 Use Cases

- Monitor power usage of appliances like water heaters, HVAC, washing machines, etc.
- Trigger automations when devices turn on or off based on current draw
- Track daily/weekly energy patterns

---

## 📸 Media

![Sap Board](images/sap-board-top.jpg)
*A close-up of the Sap AC Measurement Expansion Board*

---

## 🛒 Available From

Visit [sprig-labs.com](https://sprig-labs.com) to learn more or purchase this module.

---

## 📚 Part of the SprigStack Ecosystem

SprigStack is a modular system of PCBs built for makers and smart home developers, including:

- Sprig – ESP32-C3 Development Board  
- Bloom – RGB LED Matrix Display  
- Root – Plant Environmental Sensor  
- Thorn – Dual MOSFET Controller  
- Branch – Smart AC Relay Switch  
- **Sap** – AC Measurement Module

---

## 📄 License

This project is open-source and licensed under the MIT License.

---

## 🙌 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you’d like to improve or suggest.

---

**Sprig Labs – Where Your Ideas Grow.** 🌱
```

---

Let me know if you'd like a version tailored for Tindie documentation or want help writing similar README files for your other boards!
