# Module 1: Sensing & AC Control

**Primary Aim:** Monitor real-time room occupancy and directly toggle the physical state of the air conditioner.

## Sub-Modules & Objectives

### Sub-Module 1.1: Motion Detection & Timeout Tracking
* **Objective:** Read input from the PIR sensor, filter out false positive noise, and run a non-blocking hardware/software timer.
* **Key Logic:** Reset the internal timer every time motion is detected. If no motion is detected for the defined threshold (e.g., 15 minutes), trigger an idle timeout flag.

### Sub-Module 1.2: AC Signal Transmission
* **Objective:** Interface with an IR transmitter (or relay switch) to dispatch turn-OFF and turn-ON commands to the AC unit.
* **Key Logic:** Translate system commands into raw IR signals (or GPIO pin state changes) and maintain an internal record of whether the AC is currently ON or OFF.

## Target Deliverables
* `ac_sensor.h` & `ac_sensor.cpp` driver files.
* Function `bool isOccupied()` returning live PIR state.
* Function `bool checkTimeout()` indicating whether inactivity period has expired.
* Function `void setACState(bool state)` triggering physical relays/IR signals.
