# Dual-Direction-Entry-Exit-Counter-Using-Decade-Up-Down-Counter-and-BCD-to-7-Segment-Decoder


This project implements a simple **people counter** circuit using **digital logic ICs**. It counts people entering and exiting a room, compares the number with a preset limit, and activates a warning LED when the count reaches the limit.

## 🧠 Project Overview

- Count the number of people entering/exiting.
- Display the count using two 7-segment displays (00–99).
- Set a **maximum allowed number** of people via DIP switches.
- Use **IC 74LS85** comparators to compare current count and preset value.
- When current count equals preset, an **LED lights up** as a visual alert.

---

## ⚙️ Features

- 🔢 **Real-time counting**: Use push buttons (or sensors) to simulate entry and exit.
- 💡 **LED Alert**: Lights up when current number of people equals preset number.
- 🔄 **Resettable**: Manual reset functionality can be added easily.
- 🔌 **Fully combinational**: Built using logic ICs — no microcontroller or code needed.

---

## 🔧 Hardware Components

| Component         | Quantity | Description                                |
|------------------|----------|--------------------------------------------|
| IC 40192         | 2        | BCD Up/Down Counter                        |
| IC 7447          | 2        | BCD to 7-segment Decoder                   |
| IC 74LS85        | 2        | 4-bit Binary Comparator (for count vs preset) |
| IC 74LS04/74LS32 | 1–2      | NOT/OR logic as needed                     |
| DIP Switch       | 1        | To set the maximum allowed people count    |
| 7-Segment Display| 2        | Common anode displays for number output    |
| LED              | 1        | Lights up when threshold is reached        |
| Push Buttons     | 2        | One for Entry, one for Exit                |
| Resistors        | ~10      | For LEDs, switches, and pull-downs         |

---

## 🔌 Working Principle

1. **People Counter Logic**:
   - Two push buttons represent entry and exit triggers.
   - IC 40192 (Up/Down Counter) handles incrementing and decrementing.
   - The current count (0–99) is sent to IC 7447 for decoding.
   - The decoded output is displayed on 7-segment displays.

2. **Setting Maximum People Limit**:
   - A DIP switch lets the user select a target number (preset limit).
   - This value is input to the **A side** of two cascaded 74LS85 comparators.

3. **Comparison & LED Warning**:
   - The current count from 40192 is connected to the **B side** of the comparators.
   - When the values **match**, the comparator output becomes active.
   - This output drives an **LED** to indicate the limit has been reached.

---

## 📌 Notes

- You can add an optional **buzzer** for audible alert when the LED is on.
- The current design assumes **manual control**. In a real application, replace buttons with IR or ultrasonic sensors.
- The circuit can be extended to:
  - Include auto-reset after threshold breach.
  - Support more digits for larger capacity.

---

## 🧠 Skills Applied

- Digital logic design using **sequential and combinational circuits**.
- Application of **comparators (74LS85)** for real-time threshold logic.
- Practical use of **BCD counters and decoders**.
- Simulation and troubleshooting in **Proteus**.

---

## 🛠️ Tools Used

- **Proteus** – Circuit simulation and testing.
- **Basic Logic ICs** – 40192, 7447, 74LS85, 74LS04, etc.

---


