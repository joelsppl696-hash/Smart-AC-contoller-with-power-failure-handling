# Smart AC Controller — Project Overview & Team Task Split

## Problem Statement
Modern educational institutions experience high electricity wastage due to unmonitored air conditioning. AC units frequently remain ON in unoccupied classrooms, staff rooms, and after office hours. Additionally, during power outages, AC units automatically resume operation upon power restoration—even in empty rooms. The lack of event logging makes energy auditing and tracking wastage virtually impossible.

## Proposed Solution
The Smart AC Controller is an ESP32-based automation and logging system. It monitors room occupancy via a PIR sensor, enforces post-office-hour shutdowns via a Real-Time Clock (RTC), prevents power-restoration AC restarts in vacant rooms using a battery-backed sensing system, and writes all events with timestamps to an SD card for continuous energy auditing.

## Team Module Matrix

| Module | Core Domain | Lead Responsibility | Primary Hardware |
| :--- | :--- | :--- | :--- |
| **Module 1** | Sensing & AC Control | Occupancy tracking & physical AC triggering | PIR Sensor, IR Blaster / Relay |
| **Module 2** | Timekeeping & Scheduling | Clock sync & office-hours policy enforcement | DS3231 RTC Module |
| **Module 3** | Data Logging & Storage | CSV event logging & SD storage handling | MicroSD Card Reader |
| **Module 4** | Power & System Integration | Mains detection, power restoration logic & main loop | Mains Voltage Sensor, Power Bank, ESP32 |

---

## File Map
* [`module_1_sensing_and_control.md`](./module_1_sensing_and_control.md) — Occupancy & AC Actuation Specifications
* [`module_2_rtc_and_scheduling.md`](./module_2_rtc_and_scheduling.md) — Real-Time Clock & Schedule Engine Specifications
* [`module_3_data_logging.md`](./module_3_data_logging.md) — File System & CSV Audit Trail Specifications
* [`module_4_power_and_integration.md`](./module_4_power_and_integration.md) — Mains Sensing & Master Integration Specifications
